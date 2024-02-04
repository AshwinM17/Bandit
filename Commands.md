# level 0-
```
 ssh bandit0@bandit.labs.overthewire.org -p 2220

```
with pass bandit0


 # level 0-1 /bandit0
 ```
 ls

 cat readme
 ```
 Pass in bandit0
```
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```

# level 1-2/bandit1
```
cat ./-  it(./) means look for the following file in the current directory
``` 
 Pass in bandit1
```
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

# level 2-3/bandit2

```
bandit2@bandit:~$ cat spaces\ in\ this\ filename 

bandit2@bandit:~$ cat "spaces in this filename" 

```
 Pass in bandit2
```
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
# level 3-4/bandit3
```
bandit3@bandit:~$ cd inhere

bandit3@bandit:~/inhere$ ls
// shows nothing.

bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden

cat ./.hidden

or
cat <.hidden

or
cat ".hidden"

```
Pass in bandit3
```
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
# level 4-5/bandit4
```
cd inhere

file ./* 
(./ for in this directory  and * for all and we use file command)
```
Pass in bandit4
```
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
# level 5-6/bandit5
```
cd inhere 

// show that all files contains various files so it is not possible to brute force it

find ./ -type f -size 1033c

returns the path to the exact file
./maybehere07/.file2

cat ".file2"

```
Pass in bandit5
```
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
# level 6-7/bandit6
```
find / -user bandit7 -group bandit6 -size 33c

//returns a list of all the files stored on the server
//we observe the fact that there is only one where it does not say permission denied

cat /var/lib/dpkg/info/bandit7.password


```
Pass in bandit6
```
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
# level 7-8/bandit7
```
$ls
 data.txt
$file data.txt
 Unicode text, UTF-8 text
$cat data.txt
//gives very long text  output

//to search for pass next to word millionth 
grep millionth data.txt

```
Pass in bandit7
```
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
# level 8-9/bandit8
```
ls 
file data.txt
cat data.txt
//gives very long text  output

cat data.txt | sort |uniq -u
or
sort data.txt | uniq -u
//uniq -u searches for unique in i-1 and i+th line that is why we had to sort

```
Pass in bandit8
```
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
# level 9-10/bandit9

```
// first show strings data.txt
strings data.txt | grep ==
O/P:-

    x]T========== theG)"
    ========== passwordk^
    ========== is
    ========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
Pass in bandit9
```
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
# level 10-11/bandit10
```
cat data.txt
or 
base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

```
pass in bandit10
```
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
# level 11-12/bandit11

```
get a rot 13// encoded file
$ cat data.txt | tr [A-Za-z] [N-ZA-Mn-za-m]
or
$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

```
pass in bandit11
```
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```


