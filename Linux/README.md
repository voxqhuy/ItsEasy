# Linux


## Basic

* Navigation
```
./Documents
../../
```

* Universal Cancel  
**Ctrl + c**   

* List items
```
ls [options] [location]
```

* Print working directory
```
pwd 
```

* Change Directories 
```
cd 
```
* Check a file's type
```
File [path] 
```

* Read manuals of a command
```
man <command>
```

* Search for all manual pages containing the given search term
```
man -k <search term> 
```
    
* Search
```
'/' <search term> enter
```

Press key **n** for search next  

* Paste something  
**Right mouse click**
      
* Quit  
Key **q**
    
* Others

Asterisk **\***  represents zero or more characters. 
*Example:*
```
ls b*
barry.txt blah.txt bob  
```

Question mark **\?**  represents a single character.      
*Example:* 
```
ls ?i* 
firstfile video.mpeg  
```

Brackets **[]**   represents a range of characters.   
*Example:* 
```
ls [sv]*  
secondfile video.mpeg
ls *[0-9]* 
foo1 foo2 foo3  
```


## File manipulation

* Creating a directory
```
mkdir [options] <Directory> 
```
 
* Remove directory
```
rmdir [options] <Directory> 
```
 
**Options:** 
Make parent directories as needed  
```
-p
```
*Example:*  
```
mkdir -p abc/hello
```
*This will create a folder 'abc' and then the file 'hello'*


+ Show what the command is doing
```
-v
```
*Example:*
```
mkdir -pv voxqhuy/foo
mkdir: created directory 'voxqhuy/foo'
```

* Remove a file
```
rm [options] <file> 
```
    
* Removing non empty Directories
```
rm -r <directory> 
```
      
* Creating a Blank File
```
touch [options] <filename>
```
 
* Copying a File 
```
cp [options] <source> <destination> 
```
*If the destination is to a file, it will create a copy of the source but name the copy the filename specified in destination.*  
*If we provide a directory as the destination then it will copy the file into that directory and the copy will have the same name as the source.*

* Copying a Directory
```
cp -r <source> <destination> 
```
**-r** is short for **recursive**  

* Move a file or a directory
```
mv [options] <source> <destination>
```
*Example:*  
```
mv foo2 backups/foo3
```
*We moved the directory foo2 into the directory backups and renamed it as foo3.*
```
mv barney backups/
```
*We moved the file barney into backups. As we did not provide a destination name, it kept the same name.*


## General rules:

**Case sensitive. No Undo. Tab for suggesting. No mouse.**  
On a Linux system there are only 2 people usually who may change the permissions of a file or directory. The owner of the file or directory and the root user. The root user is a superuser who is allowed to do anything and everything on the system. Typically the administrators of a system would be the only ones who have access to the root account and would use it to maintain the system. Typically normal users would mostly only have access to files and directories in their home directory and maybe a few others for the purposes of sharing and collaborating on work and this helps to maintain the security and stability of the system.  

* File names with spaces  
```
Holiday Photos
```
Use 'Holiday Photos' or Holiday\ Photos

* Hidden files  
The dot **'.'**   
```
.file.txt
```
To show hidden files: Use **-a** (stands for 'all')
```
ls -a
```

* Shorthand commands
```
ls -a  
ls -alh(combined)
```

* Longhand commands
```
ls --all
```

## Vi Text Editor
* Start Vi
```
vi <file>
```
 
* View small files
```
cat <file>
```

* View big files    
```
less <file>
```
*Usages:*
**SpaceBar** forward a page  
Key **b** back a page  
Key **q** quit

### Insert mode
* Enable Insert mode
Key **i**

* Escape Insert mode (generally a no-harm key in Vi)
Key **Esc**

### Edit mode
* Save and exit
```
ZZ
```
or
```
:wq
```

* Discard all changes, since the last save, and exit
```
:q!
```

* Save file but don't exit
```
:w
```

* Delete a character
```
x
```

* Delete a line
```
dd
```

* Undo (keep pressing to keep undoing)
```
u
```

* Undo all changes
```
U
```
       
### Navigating in Vi   
(Type **:set nu** in edit mode to enable line numbers)  

**Arrow keys** - move the cursor around  
**^** (caret) - move cursor to beginning of current line  
**$** - move cursor to end of the current line  
**{** - move backward one paragraph  
**}** - move forward one paragraph  


## Filters
* head  
Head is a program that prints the first so many lines of it's input. By default it will print the first 10 lines but we may modify this with a command line argument.
```
head [-number of lines to print] [path]
```
```
head mysampledata.txt
Fred apples 20
Susy oranges 5
Mark watermellons 12
Robert pears 4
Terry oranges 9
Lisa peaches 7
Susy oranges 12
Mark grapes 39
Anne mangoes 7
Greg pineapples 3
```
* Tail   
Tail is the opposite of head. Tail is a program that prints the last so many lines of it's input. By default it will print the last 10 lines but we may modify this with a command line argument.
```
tail [-number of lines to print] [path]
```
```
tail -3 mysampledata.txt
Greg pineapples 3
Oliver rockmellons 2
Betty limes 14
```
* Sort
Sort will sort it's input, nice and simple. By default it will sort alphabetically but there are many options available to modify the sorting mechanism. Be sure to check out the man page to see everything it may do.
```
sort [-options] [path]
```
```
sort mysampledata.txt
Anne mangoes 7
Betty limes 14
Fred apples 20
Greg pineapples 3
Lisa peaches 7
Mark grapes 39
Mark watermellons 12
Oliver rockmellons 2
Robert pears 4
Susy oranges 12
Susy oranges 5
Terry oranges 9
```
* eGrep  
egrep is a program which will search a given set of data and print every line which contains a given pattern
```
egrep [command line options] <pattern> [path]
```
```
egrep 'mellon' mysampledata.txt
Mark watermellons 12
Oliver rockmellons 2
```
**-n** to show line numbers; **-c** to show the match counts only
```
egrep -n 'mellon' mysampledata.txt
3:Mark watermellons 12
11:Oliver rockmellons 2
egrep -c 'mellon' mysampledata.txt
2

```


## Permission

Linux permissions dictate 3 things you may do with a file, read, write and execute  
**r** read - you may view the contents of the file.  
**w** write - you may change the contents of the file.  
**x** execute - you may execute or run the file if it is a program or script.  

For every file we define 3 sets of people for whom we may specify permissions.  
**owner** - a single person who owns the file. (typically the person who created the file but ownership may be granted to some one else by certain users)  
**group** - every file belongs to a single group.  
**others** - everyone else who is not in the group or the owner.  

###### View permissions, use the long listing option -l for the command ls  
* View permissions for files
```
ls -l [path]
drwxr-xr-x 1 voxqhuy voxqhuy 512 Jul 28 01:16 voxqhuy
ls -l /home/voxqhuy/linuxtutorialwork/frog.png
-rwxr----x 1 harry users 2.7K Jan 4 07:32 /home/voxqhuy/linuxtutorialwork/frog.png
```
The first 10 characters of the output are what we look at to identify permissions.  
###### The first character identifies the file type  
If it is a dash **\-**, it is a normal file. If it is a **d**, it is a directory.  
###### The next 3 characters represent the permissions for the owner  
A letter represents the presence of a permission; a dash **-** represents the absence of a permission.  
In this example the owner has all permissions (read, write and execute)
###### The following 3 characters represent the permissions for the group
The 1st group has the ability to read and executebut not write or execute  
The 2nd group has the ability to read but not write or execute  
###### Finally the last 3 characters represent the permissions for others  

* View permission for directories  
The same series of permissions may be used for directories but they have a slightly different behaviour.   
**r** - you have the ability to read the contents of the directory (ie do an ls)  
**w** - you have the ability to write into the directory (ie create files and directories)  
**x** - you have the ability to enter that directory (ie cd)  
```
ls testdir
file1 file2 file3
chmod 400 testdir
ls -ld testdir
dr-------- 1 ryan users 2.7K Jan 4 07:32 testdir
cd testdir
cd: testdir: Permission denied
ls testdir
file1 file2 file3
chmod 100 testdir
ls -ld testdir
---x------ 1 ryan users 2.7K Jan 4 07:32 testdir
ls testdir
cd testdir
pwd
/home/ryan/testdir
ls: cannot open directory testdir/: Permission denied
```

* Change permissions
```
chmod [permissions] [path]
```
**chmod** has permission arguments that are made up of 3 components:  
Who are we changing the permission for? [ugoa] - user (or owner), group, others, all  
Are we granting or revoking the permission - indicated with either a plus ( + ) or minus ( - )  
Which permission are we setting? - read ( r ), write ( w ) or execute ( x )  
```
ls -l frog.png
-rwxr----x 1 harry users 2.7K Jan 4 07:32 frog.png
chmod g+x frog.png
ls -l frog.png
-rwxr-x--x 1 harry users 2.7K Jan 4 07:32 frog.png
chmod u-w frog.png
ls -l frog.png
-r-xr-x--x 1 harry users 2.7K Jan 4 07:32 frog.png
```
Or we can assign multiple permissions at once
```
ls -l frog.png
-rwxr----x 1 harry users 2.7K Jan 4 07:32 frog.png
chmod g+wx frog.png
ls -l frog.png
-rwxrwx--x 1 harry users 2.7K Jan 4 07:32 frog.png
chmod go-x frog.png
ls -l frog.png
-rwxrw---- 1 harry users 2.7K Jan 4 07:32 frog.png
```
* Setting Permissions Shorthand  
*This is a little advanced.*
For example **1** = **--x**; **7** = **rwx**  

d | r w x  
0 |	0 0 0  
1 |	0 0 1  
2 |	0 1 0  
3 |	0 1 1  
4 |	1 0 0  
5 |	1 0 1  
6 |	1 1 0  
7 |	1 1 1  
```
ls -l frog.png
-rw-r----x 1 harry users 2.7K Jan 4 07:32 frog.png
chmod 751 frog.png
ls -l frog.png
-rwxr-x--x 1 harry users 2.7K Jan 4 07:32 frog.png
chmod 240 frog.png
ls -l frog.png
--w-r----- 1 harry users 2.7K Jan 4 07:32 frog.png
```
