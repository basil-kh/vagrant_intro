# Bash and Linux commands

Create a file
```bash
touch example.txt
```
Move or rename files (the file will retain its original type)
```bash
mv <file> <newfile>
```
note:
- Linux is case sensitive 

read file:
```bash
cat <file>
```
open and edit file:
```bash
sudo nano <file> or nano <file>
```
ctrl x + y + enter -- when you are done edititing file

this will also make the file if that file does not exist and put your content in it

----------------------------------------------------------------
Make a folder:
```bash
mkdir <folder1> <folder2> ....
```
don’t use space in file name or you will have to use “” initially and every time you want to enter that file

---
deletes file (removes):
```bash
rm <filename>
```


**warning!** : **never** do rm -rf, it will delete the entire system 

-rf forces the delete even if file is open :
```bash
rm -rf <filename>
```


---
makes hiddenfolder or file just add . infront:
```bash
mkdir .<foldername>
```


show all files including hidden 
```bash
ls -al
```


more information than -al including permissions
```bash
ls -all
```

wildcard will show certain files:
```bash
ls <startoffilename>*
ls *<endoffilename eg .txt>
```
Show permissions:
```bash
ls -l 
```
permissions r-read w-write x-execute:




```bash
drwxrwxr-x 2 vagrant vagrant 4096 May 10 15:11 documents
-rw-r--r-- 1 root    root      25 May 10 15:05 example2.txt
-rw-rw-r-- 1 vagrant vagrant   47 May 10 15:05 example3.txt
-rw-rw-r-- 1 vagrant vagrant   25 May 10 15:03 example.txt
```
1. first rw is owner who made the file
2. second is a group 
3. third is everyone else
---
gives everyone permission to execute a file:
```bash
cdmod u+x example.txt
```
permissions after:
```bash
drwxrwxr-x 2 vagrant vagrant 4096 May 10 15:11 documents
-rw-r--r-- 1 root    root      25 May 10 15:05 example2.txt
-rw-rw-r-- 1 vagrant vagrant   47 May 10 15:05 example3.txt
-rwxrw-r-- 1 vagrant vagrant   25 May 10 15:03 example.txt
```

gives everyone permission to anything to the file:
```bash
sudo chmod 777 example.txt
```
permissions after:
```bash
drwxrwxr-x 2 vagrant vagrant 4096 May 10 15:11 documents
-rw-r--r-- 1 root    root      25 May 10 15:05 example2.txt
-rw-rw-r-- 1 vagrant vagrant   47 May 10 15:05 example3.txt
-rwxrwxrwx 1 vagrant vagrant   25 May 10 15:03 example.txt
```



A permissions calculator -- [https://chmod-calculator.com/](https://chmod-calculator.com/)