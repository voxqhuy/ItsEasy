# Fast Tutorials for ... everything

###### Favored audience: sexy Geeks
This is my collection of quick tutorials for popular developers' tools.  
I personally edit and summarize to keep the content as concise as possible.  
*(**Suggestions** are appreciated; **contributions** are more than welcomed)*

## Table of Contents

- [Linux](#linux)
- [Regex](#regex)

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


## Permission

* To view permissions for a file we use the long listing option **-l** for the command ls
```
ls -l [path]
drwxr-xr-x 1 voxqhuy voxqhuy 512 Jul 28 01:16 voxqhuy
```
      
## General rules:

**Case sensitive. No Undo. Tab for suggesting. No mouse.**
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


# Regex

```
abc…	Letters
123…	Digits
\d	Any Digit
\D	Any Non-digit character
.	Any Character
\.	Period
[abc]	Only a, b, or c
[^abc]Not a, b, nor c
[a-z]	Characters a to z
[0-9]	Numbers 0 to 9
\w	Any Alphanumeric character
\W	Any Non-alphanumeric character
{m}	m Repetitions
{m,n}	m to n Repetitions
*	Zero or more repetitions
+	One or more repetitions
?	Optional character
\s	Any Whitespace
\S	Any Non-whitespace character
^…$	Starts and ends
(…)	Capture Group
(a(bc)) Capture Sub-group
(.*)	Capture all
(abc|def) Matches abc or def
```

# References

* [Ryans Tutorials](https://ryanstutorials.net/linuxtutorial/)
* [RegexOne](https://regexone.com//)
