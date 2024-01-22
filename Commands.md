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
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
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

```
