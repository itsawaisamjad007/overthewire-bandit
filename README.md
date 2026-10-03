# Over the wire bandit :-
---
### NOTE :

* Read instructions and tips given in official web before every level about it . It is very helpful to solve
  this levels. 
* I hide the passwords which I finds, due to security guidlines and restrictiond so any one find it by own, and get 
  Practice by facing failures and solve them, which is very good practice.

## Level 0 - 1 :-

### Objective :

Find Password for level 1.

### Official web given guides :

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.


 
### Connection command :

ssh bandit0@bandit.labs.overthewire.org -p 2220

### Tool Used :

Kali Linux

### Screenshot:

![Enter Level 1](./Screenshots/Access%20level%201.png)



### Investigation :

* First enter level 1 using terminal of kali linux and enter default command and default password.
* Then I run ls command to check list of file folder.
* There was only one file named readme.
* Then i simply use cat command to show the content of readme file and I find Password for next level.

### Commands Used :

* ls
* cat

-------


## Level 1 - 2 :-

### Objectives :
To find password for Level 2

### Official Web given guides :

The password for the next level is stored in a file called - located in the home directory.

### Connection Command :

ssh bandit1@bandit.labs.overthewire.org -p 2220

### Investigation :
* First of all I use ls command in home directory to list files and folder .
* Where I see that there is a file named by special character.

### Failure :

* I use command ' cat - ' and which did't show any result.
* Then I use ' cat "-" which also did't show any result .

### Why I success to open this file :

* Then I use Google for help and came to know that special character name files open in different way than 
  simple one.
* Which was ' cat ./- ' and then I successfully open that file and note the password for next level entry.

### Command Used :
* ls
* cat ./-

### Final Learning:

* To open file name by using special character in open by using 
  cat ./(S.C)

## Level 2 - 3 :-

### Official Web given guidence :

The password for the next level is stored in a file called --spaces in this filename-- located in the home directory.

### Connection Command :

ssh bandit2@bandit.labs.overthewire.org -p 2220

### Investigations :
* First of all I use ls command 
* Then I tried simple cat command to open file, but failed many time .

### Screenshot :

![](./Screenshots/Attempt%20to%20show%20file.png)

### Searches :

* Then I search google and I came to know that file name with spaces can be open in different way, using 
  options. 
* Then I run cat -- "--spaces in the filename--" 

![](./Screenshots/Run%20correct%20command.png)


### Result :

Then I successfuly open the file and note the password.

### Final Learnings :

* When the given file name is using spaces, it will open by using 
  cat -- "Name File"


## Level 3 - 4 : 

### Official Web :
The password for the next level is stored in a hidden file in the inhere directory.

### Connection Command : 

ssh bandit3@bandit.labs.overthewire.org -p 2220

### Investigations :
* First of all I use ls command.
* Then I use ls -la command in inhere directory.

### Failures :
* First of all I simply use cat command to open file
* Then I use the same format in it as 
   cat -- "File-Name"


### Screenshot:
![](./Screenshots/Level%203%20find.png)

### Result : 
* Then finally I note the password .

### Command Used :
* ls -la
* cat -- "file-name"

### Final Learnings: 

* I finally learn from this level, that if file name is seperated by hiphe, then it is also open 
  by using options like cat -- "file-name" .


## Level 4 - 5 :-

### Official Web given guidence :
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

### Connection Command :
ssh bandit4@bandit.labs.overthewire.org -p 2220

### Investigations :
* First of all I use ls command to show directries .
* Then I use file command to check the type of files

### Screenshot :
![](./Screenshots/Level%204%20part%201.png)

---
### Failure :

* I fail many time to find human readable command.
* Then I run file ./* and find that -filexx is targetted file


---


![](./Screenshots/level%204%20part%202.png)


### Result :

* At last I use cat ./file07 command to open file and I note the password

### Command Used :
* ls 
* cd 
* file ./dir *
* cat ./-filexx

### Final Learning :

* In this level, I learn using file command to check the type of files of directory at one
* I also learn , how file name start with special character , to open
