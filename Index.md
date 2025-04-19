# Chapter 1- Introduction

Linux is an open-source operating system, just like UNIX, that powers a
wide range of devices, from servers to smartphones. It offers stability,
security, and customization, with a command-line interface for advanced
control. Distros like Ubuntu, Fedora, and Debian provide various
user-friendly versions, while developers can access the kernel source
for customization.

A user can interact with Linux either using a **graphical interface** or
using the **command line interface**.

## Operating system

It is made of three parts:

### 1- Programs

A user executes programs. AngryBird is a program that gets executed by
the kernel, for example. When a program is launched, it creates
processes. Program or process will be used interchangeably.

### 2- The Kernel

-   The Kernel handles the main work of an operating system.
-   Allocates time & memory to programs
-   Handles File System
-   Responds to various Calls

### 3- The Shell

A user interacts with the Kernel via the Shell. A user writes
instructions in the shell to execute commands. Shell is also a program
that keeps asking you to type the name of other programs to run.

## Linux files and processes

Everything in Unix is either a file or a process.

### Process

When we run a program, a process is created. Every process is identified
by a number called process ID. To check the processes you are running,
execute “ps” command on the shell. You can think of the process ID to be
a sequence number given by the operating system. It may be different at
different execution of the same program.

### File

-   A file is a sequence of data. A file could be created by users using
    word processors or text editors or by the program to keep the
    information. A program is kept in the form of a file and when it is
    run by the kernel, it loads as a process.

-   A file is generally written on the disk so that it exists even after
    the computer restarts. It is saved in a disk - either **hard disk
    drive (HDD - cheaper and slower)** or **solid state drive (SSD -
    faster but costlier)**.

-   A file is identified by a name called file path. In Unix, everything
    is represented as file:

    -   Devices such as Mouse, Keyboard
    -   Programs are saved as file
    -   Disk and Monitor

## Linux file system Hierarchay

A file is kept inside a directory. A directory can have a file or
another directory inside it. It is like an inverted tree.

-   The top level directory is **“/” called root**. “/” directory does
    not have a parent.

-   /usr/tmp means tmp is inside usr which is inside top level directory
    “root”.

<img src="Figures/Directory.png" width="1600" style="display: block; margin: auto;" />

###### Image Source: <https://www.serverkaka.com/2018/01/key-locations-in-linux-file-system_21.html>

# Important LINUX commands

## pwd

-   Tells the current working directory

<table>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>pwd</strong></td>
<td>print the path of current directory</td>
<td>pwd</td>
<td>/home/sandeep</td>
</tr>
</tbody>
</table>

## cd

-   Use to change the directory

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cd</strong></td>
<td>change the directory</td>
<td>cd /mnt/d/UNIX</td>
<td><a href="mailto:sandeep@DESKTOP-AVG9Q5A"
class="email">sandeep@DESKTOP-AVG9Q5A</a>:/mnt/d/UNIX</td>
</tr>
<tr class="even">
<td><strong>cd ..</strong></td>
<td>Go back to one directory</td>
<td>cd ..</td>
<td><a href="mailto:sandeep@DESKTOP-AVG9Q5A"
class="email">sandeep@DESKTOP-AVG9Q5A</a>:/mnt/d/</td>
</tr>
<tr class="odd">
<td><strong>cd -</strong></td>
<td>Return to previous directory</td>
<td>cd -</td>
<td><a href="mailto:sandeep@DESKTOP-AVG9Q5A"
class="email">sandeep@DESKTOP-AVG9Q5A</a>:/mnt/d/UNIX</td>
</tr>
<tr class="even">
<td><strong>cd ~</strong></td>
<td>Return to home directory</td>
<td>cd ~</td>
<td><a href="mailto:sandeep@DESKTOP-AVG9Q5A"
class="email">sandeep@DESKTOP-AVG9Q5A</a>:~$</td>
</tr>
</tbody>
</table>

## whoami

-   Use to find the user name

<table>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>whoami</strong></td>
<td>find user name</td>
<td>whoami</td>
<td>sandeep</td>
</tr>
</tbody>
</table>

## uname

-   Use to find the operating system name

<table>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>uname</strong></td>
<td>find operating system name</td>
<td>uname</td>
<td>Linux</td>
</tr>
</tbody>
</table>

## ls

-   Use to list the files and directories

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ls</strong></td>
<td>List files and directories in the current directory</td>
<td>ls</td>
<td>Dir1 file1 Dir 2 file2</td>
</tr>
<tr class="even">
<td><strong>ls -l</strong></td>
<td>long listing format</td>
<td>ls -l</td>
<td>drwxr-xr-x 1 sandeep sandeep 512 Aug 2 10:54 Dir1</td>
</tr>
<tr class="odd">
<td><strong>ls -a</strong></td>
<td>to show hidden file (. or ..)</td>
<td>ls -a</td>
<td>.bashrc dir1 file1 dir2</td>
</tr>
<tr class="even">
<td><strong>ls -lt</strong></td>
<td>t tells more recent files</td>
<td>ls -lt</td>
<td>-rwxr-xr-x 1 sandeep sandeep 25 Aug 9 21:15 first_script.sh</td>
</tr>
<tr class="odd">
<td>ls *.sh</td>
<td>display all sh files in current directory</td>
<td>ls *.sh</td>
<td>first.sh try.sh</td>
</tr>
<tr class="even">
<td><strong>ls -l /mnt/d/UNIX/</strong></td>
<td>can be used for different folder using path too</td>
<td>ls -l /mnt/d/UNIX/</td>
<td>dir_unix file_unix</td>
</tr>
</tbody>
</table>

## man

-   Provides comprhensiv manual for a specific command.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>man ls</strong></td>
<td>shows all commands specific to function here for ls</td>
<td>man ls</td>
<td>ls related commands</td>
</tr>
</tbody>
</table>

## mkdir

-   Use to create a new directory

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>mkdir</strong></td>
<td>make new directory</td>
<td>mkdir test1</td>
<td>test1</td>
</tr>
<tr class="even">
<td><strong>mkdir D1 D2</strong></td>
<td>make multiple directories</td>
<td>mkdir D1 D2</td>
<td>D1 D2</td>
</tr>
<tr class="odd">
<td><strong>mkdir -p dir1/dir2</strong></td>
<td>make dir1 directory with dir2 subdirectory</td>
<td>mkdir -p dir1/dir2</td>
<td>dir2 inside dir1</td>
</tr>
</tbody>
</table>

## cp

-   use to create a copy of

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Commands</strong></th>
<th><strong>Explanation</strong></th>
<th><strong>Example</strong></th>
<th><strong>Output</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cp file.txt /path/to/destination/</strong></td>
<td>copy file from one directory to another</td>
<td>~/DIR1$ cp trial.txt /home/sandeep/DIR2</td>
<td>trial.txt inside DIR2 now</td>
</tr>
<tr class="even">
<td><strong>cp file1.txt file2.txt /path/to/destination/</strong></td>
<td>Copying Multiple Files to a Directory</td>
<td>~/DIR1$ cp F1.txt F2.txt/home/sandeep/DIR2</td>
<td>F1.txt, F2.txt inside DIR2 now</td>
</tr>
<tr class="odd">
<td><strong>cp -r Source_DIR /path/to/destination/</strong></td>
<td>Copying a Directory and Its Contents</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><strong>cp source_file.txt
/path/to/destination/new_file_name.txt</strong></td>
<td>Copying Files with a New Name:</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>cp *.txt /path/to/destination/</td>
<td>Copying Files using Wildcards (e.g., Copying all .txt files)</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## mv

Moving file from one directory to another

# File permission

-   When we create a text file, we must have to check the permission

-   When we call **ls -l** command, we see some information of each file
    or directory.

    -   For example: **-rwxrw-r– sandeep sandeep 25 Dec 23 08:26
        file\_name.txt**

-   In UNIX, permission is divided into three categories:

## Owner permission:

-   here first three after -, rwx and first sandeep (file owner)

## Group permission

-   here after rwx, we have rw- and second sandeep (group file owner)

## Others permission

-   not part of first two categories, here r–

## Characters in permission field:

        * r - read permission (can read file)
        * w - write permission (can write to the file)
        * x - execute permission (can run the file)
        * - - means person does not have that permission
        

## Changing permision

### using alphabet

-   we have to use change mode command (**chmod**)
    -   **chmod a+x file\_name.txt**
        -   Granting permission to all users. **a** means for all three
            categories change permission. **+x** means grant permission
            to execute for all three categories.
    -   **chmod a-x file\_name.txt**
        -   remove execute permission for all three categories
    -   **chmod u+x file\_name.txt**
        -   permission for file owner only. **u** means file owner
    -   **chmod g+x file\_name.txt**
        -   permission for group file owner only. **g** means group file
            owner
    -   **chmod o+x file\_name.txt**
        -   permission for other owners only. **o** means other owner

### using numeric values

-   r = 4
-   w = 2
-   x = 1
    -   maximum permission for file owner (r+w+x = 7) or any any
        specific group

    -   read permision to one group will be r = 4

        -   **chmod 644 file\_name.txt**
            -   removing execute permission from file.
                -   6 means only read and write permission to owner
                -   4 mean only read permission to group owner
                -   4 mean only read permission to others
        -   **chmod 755 file\_name.txt**
            -   7 means all three permission to owners
            -   5 means read and execute permission to group owners
            -   5 means read and execute permission to others

# Shell scripting

A sequence of system commands pasted in a file.

-   For loops
-   Conditional
-   Variables
-   Arguments
-   etc

<br> <br> - Helps to avoid same command again and again.

-   We should know use of some editors before it such as vi or anything
    else.

## Creating scripts

-   Script file is created with sh extension (**my\_script.sh**) as
    convention. We can also use bash as an extension too.

    -   creating my script **`vi my_script.sh`**
    -   This will open your editor

-   first line on any script will be **\#!/bin/bash**

-   from next line we can write our commands (ls, date, pwd)

-   Each command in separate line to avoid error.

-   \#!/bin/bash <br> pwd <br> ls <br> date

Note: here <br> means is only space

## Invoking script

./my\_script.sh - Here ./ means we will invoke the script from current
directory only.

-   We can also give whole path to run the script. Check the path with
    pwd command /path/my\_script.sh

-   We can also check if file is in the path or edit the environment of
    path

-   Display the content of path variable

    -   **echo $PATH**
    -   If directory that the script is located in the variable path we
        can invoke the script by just typing its name
    -   Otherwise we create path:
    -   **export PATH=*P**A**T**H*:(pwd)**
        -   pwd means full path of directory where it is located or your
            current directory path
        -   This will add your script in path and we can run it directly
            from same directory or ant other directory

## ShaBang

-   Why the first line of script is called ShaBang

**\#!/bin/bash** \* \# - Sharp (used in programming langauge C#) \* ! =
in slang called bang \* \#! = Together called ShaBang \* /bin/bash is to
run our script

-   We can also used **interpreter** = /bin/bash my\_script.sh
-   In this case first line is not required in .sh file. However, it is
    not recommended in real life scenario.

## Variable

-   We have 3 ways to assign a value to a variable.
    -   Explicit definition: VAR=value
    -   Read command: read VAR
    -   Command substitution: VAR = $(pwd)

### Explicit defintion

#### Creating variable

-   VAR=value (no sapces before or after equal sign)
    -   COUNT=5
    -   PATH=/var/lib
    -   DOGS\_NUMBER = 8 \# wrong
    -   MESSAGE=hello
    -   MESSAGE=hello world \# wrong
    -   MESSAGE=“hello world”

If we put space between them it will read as DOGS\_NUMBER as command,
and = & 8 as two arguments. - Variable name can be small letters too

#### Accessing variables

-   echo $COUNT
-   echo $PATH
-   echo “path = $PATH”

### Read command

-   read VAR

-   Interactive way how to set a variable

-   \#!bin/bash <br> echo -n “Enter your age:” <br> read AGE <br> echo
    “your age is $AGE” <br> <br>

-   \#!bin/bash <br> echo -n Your name: <br> read NAME <br> echo -n Your
    age: <br> read AGE <br> echo <br> echo ===Student Statistics=== <br>
    echo Name: $NAME <br> echo Age: $AGE <br> <br>

-   \#!bin/bash <br> read -p “Your name:” NAME <br> read -sp “Your age:”
    AGE <br> echo <br> echo “Name: $NAME, Age: $AGE” echo “your age is
    $AGE” <br> <br>

-   Check the hostname of your system

    -   \#!bin/bash <br> read HOSTNAME &lt; /etc/hostname <br> echo
        Hostname: $HOSTNAME

### Command Substitution

-   There are two ways:

    -   VAR=$(pwd)
        -   Set a value to variable as an output of a given command
    -   VAR=`pwd`

-   \#!/bin/bash <br> CURRENT\_DIR=$(pwd) <br> echo “Script is run from:
    $CURRENT\_DIR”

-   \#!/bin/bash <br> CURRENT\_DIR=`pwd` <br> echo “Script is run from:
    $CURRENT\_DIR”

-   How much time is taken by a specific command

-   check video 21

## Match calculation

-   let
-   (())
-   \[\]
-   expr
-   bc \# operate floating point

### let

-   \#!/bin/bash <br> NUMBER=7 <br> let RESULT=NUMBER+5

    -   Increment operation: let NUMBER++  
        \# (let NUMBER+=5) –&gt; let NUMBER = NUMBER + 5
    -   Decrement Operations: let NUMBER–  
        \# (let NUMBER-=5) –&gt; let NUMBER = NUMBER - 5

### (())

-   RESULT=$(( NUMBER + 5 ))

### \[\]

-   RESULT=$\[NUMBER + 5\]

### expr

-   RESULT=$(expr $NUMBER + 5)
-   RESULT=`expr $NUMBER + 5`

### bc

-   operating with floating point
    -   RESULT=`echo "$NUMBER * 1.9" | bc`
-   RESULT=`expr 2 + 3`

IMP: `set nu` gives number to vi editor

## Arguments

-   Passing arguments into script
-   Passing arguments to function
-   Example of calling a script with three arguments:
    -   ./arguments one two three

### Arguments - accessing them from script

-   $0 - script name

-   $1 - first argument

-   $2 - second argument

-   $n - nth argument

-   “$@” - all arguments, expands as “$1” “$2” “$3” and so on

-   “$\*” - all arguments, expands as one string “$1c$2c$3”, where c is
    the first character of IFS (internal field separator) <br> Firs
    character of IFS is usually a space

-   $# - argument count

-   file name vi arguments.sh

-   \#!/bin/bash <br> <br> echo “Script name: $0” <br> echo “First
    argument: $1” <br> echo “Second argument: $2” <br> echo “All
    arguments with $@: $@” <br> echo “All arguments with $*: $*” <br>
    echo “Arguments count: $#”

-   ./arguments.sh one 2 three

### Internal Field separator (IFS)

-   file name vi arguments.sh

-   \#!/bin/bash <br> <br> IFS=“,” <br> echo “Script name: $0” <br> echo
    “First argument: $1” <br> echo “Second argument: $2” <br> echo “All
    arguments with $@: $@” <br> echo “All arguments with $*: $*” <br>
    echo “Arguments count: $#”

-   ./arguments.sh one 2 three four

<br> <br> - vi arguments2.sh

-   \#!/bin/bash <br> <br> \# assign arguments value to a variable <br>
    FIRST=$1 <br> SECOND=$2
    &lt;br&gt;
    let RESULT=FIRST+SECOND
    &lt;br&gt;
    echo "$FIRST + $SECOND = $RESULT”

-   ./arguments2.sh 2 5

## Redirecting and Piping

-   Every program we run on the command line automatically has three
    data streams.

    -   STDIN (0) - Standard input (data provided to program)
    -   STDOUT (1) - Standard output (what program prints, default to
        the terminal)
    -   STDERR (2) - Standard error (what error messages program prints,
        default to the terminal)

-   STDIN(0) provides some data into programm (wc, cat, ping etc). If
    there is no issue program will provide STDOUT(1) and if there is an
    issue it will provide output as STDERR(2).

-   Examples:

    -   cat files1.txt &gt; output\_from\_cat.txt (by defautl it will
        direct to STDOUT)
    -   cat files1.txt 1 &gt; output\_from\_cat.txt (redirect to STDOUT)
    -   cat files1.txt 2 &gt; errors.txt (redirect to STDERROR)
    -   cat files1.txt 1 &gt; output\_from\_cat.txt 2 &gt; errors.txt
    -   cat files1.txt & &gt; output\_from\_cat.txt (bith STDOUT AND
        STDERROR)
    -   cat files1.txt 1 &gt; output\_from\_cat.txt 2&gt;&1 (STDERROR to
        STDOUT)

#### Redirection

-   wc -l file.txt
    -   12 file.txt
-   wc -l &lt; file.txt
    -   12

#### Piping

-   Sending data fromo one program to another
-   cat file.txt | wc -l
-   cat file.txt | (wc -l &lt; file.txt
-   cat file.txt | head -5 | tail-3| wc -l

NOTE: check redirecting and piping showcase video

## Exit staus

-   A numerical value which will tell us if previously called script or
    executed command is successful or not.
    -   echo $?
        -   $? will give a return value of previous command
        -   the return value is called **exit status**
    -   If the command exits successfully, exit status will be 0,
        otherwise some **non-zero** value.
    -   We can exit a script using **exit** command.
        -   echo “hello buddy”
        -   echo$?
        -   let VAR=5\*5
        -   echo$?
        -   let VAR=5\*string
        -   echo$?
        -   let VAR=5\*5; echo $VAR
-   Example
    -   \#!/bin/bash VAR=1 <br> let VAR++ <br> let VAR++ <br> echo “var:
        $VAR” <br> <br> let VAR++ <br> let VAR++ <br> echo “var: $VAR”
        <br> <br> let VAR++ <br> let VAR++ <br> echo “var: $VAR” <br>
-   Example
    -   \#!/bin/bash VAR=1 <br> let VAR++ <br> let VAR++ <br> echo “var:
        $VAR” <br> <br> let VAR++ <br> let VAR++ <br> echo “var: $VAR”
        <br> exit 1 <br> let VAR++ <br> let VAR++ <br> echo “var: $VAR”

# If else

if \[ conditon \]; then <br> statements for when the condition is true
<br> elif \[ condition \]; then <br> statements for when the condition
is true <br> elif \[ condition \]; then <br>  
statements for when the condition is true <br> else <br> statements for
when the no previously typed conditions were true

### Using logical operators

-   **&&**: when both conditions are true
-   **||**: when at least one condition is true
-   **!**: negating the given conditions

### Conditions

-   Mathematical comparison
-   String comparison
-   Filesystem related tests

## Mathematical compariosn

-   operands
    -   **-eq** equal to
    -   **-ne** not equal to
    -   **-gt** greater than
    -   **-lt** less than
    -   **-ge** greater than or equal too
    -   **-le** less than or equal too
-   Examples:
    -   if \[ $VAR -eq 5 \]; then
    -   if \[ $VAR -gt 7 \]; then
    -   if \[ $VAR -eq 5 \] && \[ $COUNT -ne 1\]; then
