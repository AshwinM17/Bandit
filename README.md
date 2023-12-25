# Bandit
login:- ssh bandit0@bandit.labs.overthewire.org -p 2220

//change the level number
<h2>bandit0</h2>
<img src="pics/Screenshot 2023-12-25 104714.png">
passwrd by writing cat readme

<b>NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL</b>

exit -d 

to exit this
and 
login:- ssh bandit1@bandit.labs.overthewire.org -p 2220
<h2>bandit1</h2>
<img src="pics/Screenshot 2023-12-25 110800.png">
When we do cat -<br>
Problem occurs as <br>
<b>Handling a Filename Starting with a Dash (-)</b>

Sometimes you can slip and create a file whose name starts with a dash (-), like -output or -f. That's a perfectly legal filename. The problem is that UNIX command options usually start with a dash (-). If you try to type that filename on a command line, the command might think you're trying to type a command option.

In almost every case, all you need to do is "hide" the dash from the command. <b>Start the filename with ./ (dot slash)</b>. This doesn't change anything as far as the command is concerned; ./ just means "look in the current directory" (1.21). So here's how to remove the file -f:
Therefore command written is:
~$ cat ./-
prints:-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
<h2>bandit2</h2>

![Alt text](pics/image.png)

Read a File with spaces in filename

You can use 'cat' command or open the document using your preferred text editor such as vim, nano or gedit.

cat 'personal docs'

Alternatively, you can use the syntax below

cat file\ name\ with\ spaces

Password:-<b>aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG</b>

<h2>bandit3</h2>



**find command used**
<p>
The find command in Linux is a dynamic utility designed for comprehensive file and directory searches within a hierarchical structure. 

find ./"directory name"

searches for all the files and returns their name also returns the file that were hidden

searches and returns all file names in the current directory


</p>
logs:

bandit3@bandit:\~*\$ ls<br>
inhere<br>
bandit3@bandit:\~*\$ cd inhere<br>
bandit3@bandit:\~*\/inhere$ ls<br>
bandit3@bandit:\~*\/inhere$ find<br>
.<br>
./.hidden<br>
bandit3@bandit:\~*\/inhere$ cat ./.hidden<br>
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe<br>
bandit3@bandit:\~*\/inhere$ #or<br>

bandit3@bandit:\~*\/inhere$ cd ~/<br>
bandit3@bandit:\~*\$ find ./inhere<br>
./inhere<br>
./inhere/.hidden<br>
bandit3@bandit:\~*\$ cat ./inhere/.hidden<br>
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe<br>
bandit3@bandit:\~*\$ <br>


Password:-<b>2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe</b>

<h2>bandit4</h2>

![Alt text](pics/image4.png)


you can use du to get size on drive,which is same,

use <b>ls -l</b> to get size ,file type which is same for eveything here
 
 so in the end I tried file ./-file00<br>
 o/p:./-file00: data
//./- as name hd - in it

same for all except -file07 which was an ascii text file

Password for bandit5:<b>lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR</b>

alternate solutions
for loop in linux for file type<br>
or <br>
cat each file and get meaningful data only in -file07

<h2>bandit5</h2>

![Alt text](pics/image5.png)

bandit5@bandit:\~\$ ls<br>
inhere<br>
bandit5@bandit:\~\$ cd inhere<br>
bandit5@bandit:\~\/inhere$ ls<br>
maybehere00  maybehere02  maybehere04  maybehere06  maybehere08  maybehere10  maybehere12  maybehere14  maybehere16  maybehere18
maybehere01  maybehere03  maybehere05  maybehere07  maybehere09  maybehere11  maybehere13  maybehere15  maybehere17  maybehere19<br>
bandit5@bandit:\~/inhere$ find . -readable -executable -size 1033c<br>

bandit5@bandit:~\/inhere$ find . -readable ! -executable -size 1033c<br>
./maybehere07/.file2<br>


Here we searched for the specifics given in the question using the find command and then mentioning the  diffrent specification so the command executed is  
**find -readable -executable -size 1033c** where c stands for bytes

Password for bandit6:**P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU**

<h2>bandit6</h2>

![Alt text](pics/imagebandit6.png)

executed:-**find / -user bandit7 -group bandit6 -size 33c**
<br>// "/ is used in find here and not above?"

![Alt text](<pics/Screenshot bandit6.png>)

found  many files,only one where permission was not denied<br>
/var/lib/dpkg/info/bandit7.password

on cat /var/lib/dpkg/info/bandit7.password

we get:**z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S**

<h2>bandit7</h2>

![Alt text](image7.png)

as we have got a text file which has a lot oof text in it 
we can use the grep command which is the search command
<h3> Grep command to search for a specific keyword and its adjacent word</h3>

command:grep millionth data.txt

it prints the line(ie till line end character) where the word millionth is present 

Password for bandit8:**TESKZC0XvTetK0S9xNwm25STk5iWrBvP**
<h2>bandit8</h2>

![Alt text](pics/image8.png)
 we had to find unique line
 so we can use **sort "filename"**
 to sort the data into alphabetical order
 and then use **| uniq -u**

 as *unique checks the **i-1th and i+1th line** and if both are diffrent rom the ith line then returns it*
 so as they are in aplhabetic order the only line printed would be the unique line(ie with frequency 1)

 ie command executed sort data.txt | uniq -u

 Password for bandit9:**EN632PlfYiZbn3PhVK3XOGSlNInNE00t**

 <h2>bandit9</h2>

![Alt text](pics/image9.png)

on cat data.txt 

we get a lot of **non-human readable text** so we have to use the <u>**strings data.txt**</u> to take out the human readable text to get the password

we can also <u>**pipe ie | grep ==**</u>

to get only those preceeded by multiple =


Password for bandit10:**G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s**

