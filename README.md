# ItsEasy

1. Commands:
+ Navigation
./Documents
../../

Ctrl + c 
      universal Cancel
Ls [options] [location]
      list items
pwd 
      print working directory
cd 
      Change Directories 
File [path] 
      what type it is
man <command>
      manuals
man -k <search term> 
      search for all manual pages containing the given search term
'q' 
      quit
'/' <search term> enter
       search, 'n' for next 

+ File manipulation
mkdir [options] <Directory> 
      Creating a directory
rmdir [options] <Directory> 
      remove directory
'-p' 
      make parent directories as needed. 'mkdir -p test/butt'
'-v'
      it is doing. 'mkdir -pv test3/butt'
rm [options] <file> 
      remove a file
rm -r <directory> 
      Removing non empty Directories

touch [options] <filename>
      Creating a Blank File
cp [options] <source> <destination> 
      Copying a File 
(If the destination is to a file, it will create a copy of the source but name the copy the filename specified in destination. If we provide a directory as the destination then it will copy the file into that directory and the copy will have the same name as the source.)
cp -r <source> <destination> 
      Copying a Dir
mv [options] <source> <destination>
(mv foo2 backups/foo3 = We moved the directory foo2 into the directory backups and renamed it as foo3)
(mv barney backups/ = We moved the file barney into backups. As we did not provide a destination name, it kept the same name.)


2. Rules:
Case sensitive. No Undo. Tab for suggesting. 
Space
      'Holiday Photos' or Holiday\ Photos
Hidden 
      '.'   .file.txt  => to show hidden files: ls -a
shorthand
      ls -a,  ls -alh(combined)
longhand
      ls --all

3. Vi Text Editor
vi <file>
      start vi
cat <file>
      view small files
less <file>
      view big files     SpaceBar=forward a page;  b=back a page; q=quit
'i'
      insert
Esc
      escape
ZZ 
      Save and exit
:q!
      discard all changes, since the last save, and exit
:w
      save file but don't exit
:wq
      again, save and exit
