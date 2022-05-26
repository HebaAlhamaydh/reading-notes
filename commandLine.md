# Command Line 

## What is Command Line?
is a user interface that's rided by typing commands at prompts.You can enter commands by writing them on the keyboard and returns will be given to you as text.

## Opening a terminal
1. On a Mac then you'll find the program Terminal under Applications -> Utilities. 
2. On Linux then you will probably find it in Applications -> System or Applications -> Utilities.
3. On Windows and intend to remotely log into another machine then you will need an SSH client

## The Shell, Bash
### Shell: 
 Is a part of the operating system that defines how the terminal will behave and looks after running commands.
 ### Bash:
 The most common shell which stands for ***Bourne again shell*** .

 shell  use a command called **echo** to display a system variable stating your current shell. echo is a command which is used to display messages.

 ## commands
 1. **pwd** : stands for ***Print Working Directory***.It tells you what your current or present working directory is
 ```
 pwd
 ```
 2. **ls**: It's short for ***list***.Show me all file in this dirctory (first layer).
 - To list the contents of my current directory 
 ```
 ls
 ```
 - list all file including hidden files.
 ```
 ls -a
 ```
 -  a long listing of the directory /etc.
 ```
 ls -l /etc
 ```
 ## Absolute and Relative Paths
 **Absolute**: paths specify a location (file or directory) in relation to the root directory.
 **Relative**: paths specify a location (file or directory) in relation to where we currently are in the system.
 
 ### Move A Round
 **cd**: which stands for change directory.

 ## obtain information about what type of file a file or directory is
 ```
 file [path]
 ```
 ## Escape Characters
 to escape (or nullify) the special meaning of the next character.
 ```
 \
 ```
 ## Hidden a File or Directory
 If the file or directory's name begins with a . (full stop).
 - To hidden a file or directory: you need to put " . " before the name.
 - To see the hidden files or directorys :
 ```
 ls -a 
 ```
 ## The Manual Pages
  a set of pages that explain every command available on your system including what they do, the specifics of how you run them, and what command line arguments they accept
  ```
  man <command to look up>
  ```
  - for ***searching***: search on the Manual pages
  ```
  man -k <search term>
  ```
  - To ***exit*** the man pages press 'q' for quit.
  ### File Manipulation
  **Making a Directory**
  ```
  mkdir [options] <Directory>
  ```
  **Removing a Directory**
  ```
  rmdir [options] <Directory>
  ```
  **Creating a Blank File**
  ```
  touch [options] <filename>
  ```
  **Copying a File or Directory**
  ```
  cp [options] <source> <destination>
  ```
  **Moving a File or Directory**
  ```
  mv [options] <source> <destination>
  ```
 **Removing a File (and non empty Directories)**
 ```
 rm [options] <file>
 ```

