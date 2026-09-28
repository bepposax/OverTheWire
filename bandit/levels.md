# Over the Wire - Bandit levels

## [0](https://overthewire.org/wargames/bandit/bandit0.html)
### Solution
Connect to ssh with username **bandit0** 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## [0 -> 1](https://overthewire.org/wargames/bandit/bandit1.html)
### Solution
Read the `readme` file in the home directory
```bash
cat readme
```
### Next
`ssh bandit1@bandit.labs.overthewire.org -p 2220`
### Password
`6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR`

## [1 -> 2](https://overthewire.org/wargames/bandit/bandit2.html)
### Solution
Read the file `-` by using the full path
```bash
cat ./-
```
### Next
`ssh bandit2@bandit.labs.overthewire.org -p 2220`
### Password
`PK8fYLZg2hnHSz83plBL1iEPKdD3QToB`

## [2 -> 3](https://overthewire.org/wargames/bandit/bandit3.html)
### Solution
```bash
cat ./"--spaces in this filename--"
```
### Next
`ssh bandit3@bandit.labs.overthewire.org -p 2220`
### Password
`7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME`

## [3 -> 4](https://overthewire.org/wargames/bandit/bandit4.html)
### Solution
```bash
cd inhere
ls -a
cat ...Hiding-From-You
```
### Next
`ssh bandit4@bandit.labs.overthewire.org -p 2220`
### Password
`xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq`

## [4 -> 5](https://overthewire.org/wargames/bandit/bandit5.html)
### Solution
```bash
file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```
```bash
cat ./-file07
```
### Next
`ssh bandit5@bandit.labs.overthewire.org -p 2220`
### Password
`6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG`

## [5 -> 6](https://overthewire.org/wargames/bandit/bandit6.html)
### Solution
```bash
cd inhere
ls
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
```
```bash
find -type f -size 1033c
./maybehere07/.file2
```
```bash
cat $(!!)
```
* The `$(!!)` shortcut recomputes the last command.  
In this case it expands to `cat $(find -type f -size 1033c)`
### Next
`ssh bandit6@bandit.labs.overthewire.org -p 2220`
### Password
`pXa26xhMWaC2SvDotA4r9EgZkulOeSBW`

## [6 -> 7](https://overthewire.org/wargames/bandit/bandit7.html)
### Solution
```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
```
* `2>/dev/null` hides all the 'Permission denied' files output
```bash
cat $(!!)
```
### Next
`ssh bandit7@bandit.labs.overthewire.org -p 2220`
### Password
`Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3`

## [7 -> 8](https://overthewire.org/wargames/bandit/bandit8.html)
### Solution
```bash
grep "millionth" data.txt
```
### Next
`ssh bandit8@bandit.labs.overthewire.org -p 2220`
### Password
`VR1ljMayciFxbnUokuQmJFw6QC9VKtub`

## [8 -> 9](https://overthewire.org/wargames/bandit/bandit9.html)
### Solution
```bash
sort data.txt | uniq -u
```
* `uniq` filters only adjacent lines. So we need to `sort` them first
* `-d` ignores duplicates and only prints unique lines
### Next
`ssh bandit9@bandit.labs.overthewire.org -p 2220`
### Password
`EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl`

## [9 -> 10](https://overthewire.org/wargames/bandit/bandit10.html)
### Solution
```bash
grep -ao "==\{2,\} \w*" data.txt
```
* `-a` reads a binary file as text
* `-o` only prints matching characters
```terminal
========== the
========== password
========== is
========== B0s2khmbT9u0geKuOoVGW3JZKhndE3BG
```
### Next
`ssh bandit10@bandit.labs.overthewire.org -p 2220`
### Password
`B0s2khmbT9u0geKuOoVGW3JZKhndE3BG`

## [10 -> 11](https://overthewire.org/wargames/bandit/bandit11.html)
### Solution
```bash
base64 -d data.txt
```
### Next
`ssh bandit11@bandit.labs.overthewire.org -p 2220`
### Password
`pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro`

## [11 -> 12](https://overthewire.org/wargames/bandit/bandit12.html)
### Solution
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
* Translate characters from alphabetic ordered input (data.exe) to the alphabet shifted by 13
![](11.png)
### Next
`ssh bandit12@bandit.labs.overthewire.org -p 2220`
### Password
`GROozWPO8QyN0mGrjUkID0WCYkZiQxrN`

<!-- ## [12 -> 13](https://overthewire.org/wargames/bandit/bandit13html)
### Solution
```bash
```
### Next
`ssh bandit13@bandit.labs.overthewire.org -p 2220`
### Password
`` -->