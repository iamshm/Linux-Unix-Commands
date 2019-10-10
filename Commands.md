<h1 align="center">Linux/Unix Commands</h1>

## Linux Commands used day to day
  `acpi`- _to display battery status and other acpi information_
  
  `apt-get` - _helps in handling packages in Linux_
  
  `arch` - _used to print computer architecture_
  
  `bc` - _used for command line calculator_
  
  `cal` -_used to see the calendar of a specific month or a whole year_
  
  `cc` - _it is used to compile C language codes and create executables_
  
  `ccrypt` - _command line tool for encryption and decryption of data_
  
   `man` - _used to give description of any linux command like this_    ```$ man ls```
  
  `info` - _an alternative toobtain uder documentation for a given program is to invoke info instead of man ```$ info ls```
  
  `mv` - _mv command is used to move or rename files_
  
  `pwd` - _shows the present working directory_

## Listing Files
- `ls`
- If you want to see the list of files on your UNIX or Linux system, use the `ls` command
- `ls -l` or `ll`
- If you want to organize the files in list
- `ls -lh`
- If you want to arrange the files in list and show their size

## Listing Hidden Files and Normal Files
- `ls -al`
- If you want ot see the list of all files with all hidden files in the Current directory system in Linux
- `ls -lha`
- If you want to organize files in list format with their sizes and see hidden files

-`ls -l`
-Displays long list view with detailed file information including file type, permissions, link count, owner, group, size, date and time

-`ls -lt`
-Lists all files sorted by date and time with the newest file first.

-`ls -ltr`
-Lists all files sorted by date and time with the oldest file first.

-`ls -lh`
-Displays all files in current directory with file sizes in human readable format(eg:1.6K,328M,2.4G)

-`ls -a`
-If you want to list all files including hidden files that start with "."

-`ls -la`
-Lists all files,including hidden files,in the current directory with detailed information.

-`ls -F`
-Displays all files in current directory with their file types.

## Creating & Viewing Files
- To create a new file, use the command
  1. `cat > filename`
  2. Add content
  3. Press `ctrl + d` to return to command prompt.
- Files can also be quickly created using
- ```echo "Hello World" > ./fileName.txt```
- To view a file, use the command `cat filename`

## Searching for content in a file/ files in a directory
- To search for a word in a file using terminal,use the command ```grep```
- For eg., if you want to search for the word GNU in a file named ```GNU.txt```,type ``` grep GNU GNU.txt```
- This will show all lines which have the word ```GNU``` in that file
- To search over multiple files in a directory, use ```grep``` with ```-r``` flag, like ``` grep -r GNU .```. Here ```-r``` stands for recursive search and ```.``` specifies the search root to be the current directory.

## Searching for a file
- `find . -name ".js" -print`: find all files with JS extnesion and print them on screen
- `find . -type d -name "*tmp" -print`: print all directories ending with `tmp`
- `find . -type f -exec ls -l {} \;`: use `ls -l` on all returned values

## Exiting the shell
- `exit` (also aliased to `bye` or `quit` in some shell flavors)

## Get root access
1. To log in as a super user use one of the following commands in the terminal. You can actually use this command to log in as any user on the machine, but when left blank it will attempt to log in as root.\
  - `su -`
  - `sudo -i`
  - These commands will ask you for password.
2. To jump right into root, run\
  - `sudo su -`
  - Since there is no root password made after live install.
3. To run other commands as root temporarily, use the command\
  - `sudo` *`command`*
  - Replace the *command* above with your command. Eg: `sudo apt-get update`

## Updating, Installing and Listing packages
The commands for installing and updating applications depend on the version of Linux you are using, specifically whether it's Debian- or RPM-based.

* Debian Based systems
  - Update the list of available packages and their versions, but doen not install or upgrade any packages. use the command ```sudo apt update```
  - Install newer versions of installed packages,use the command ```sudo apt upgrade```
  - Install any required package,use ```sudo apt install 'your package name'```. Example: ```sudo apt install apache2```

* RPM-based systems
  - Update all or specified packages,use ```sudo yum update```. Example for updating specific package: ```sudo yum update mysql```
  - Lists known and installed packages,use ```sudo yum list``` ```sudo yum list --installed```
  - Install requested package,use ```yum install```. Example: ```sudo yum -y install firefox```
  - On Fedora 22 and later, you can also use 'dnf' in place of 'yum'. dnf stands for dandified yum, and is just an updated version of yum.     	   Syntax is very similar, Examples would be: ```sudo dnf update``` or ```sudo dnf install```. More info on this [here.](https://opensource.com/article/18/8/guide-yum-dnf)

## Download YouTube videos on Linux

For this you need to install an utility called **youtube-dl**, which is a command-line program to download videos from YouTube.com and a few more sites. It requires the Python interpreter, version 2.6, 2.7, or 3.2+, and it is not platform specific. It should work on your Unix box, on Windows or on macOS. It is open source project. You can contribute [here.](https://github.com/ytdl-org/youtube-dl)

To install it right away for all UNIX users (Linux, macOS, etc.), type:

    sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
    sudo chmod a+rx /usr/local/bin/youtube-dl

If you do not have curl, you can alternatively use a recent wget:

    sudo wget https://yt-dl.org/downloads/latest/youtube-dl -O /usr/local/bin/youtube-dl
    sudo chmod a+rx /usr/local/bin/youtube-dl

It is very simple to use. Following are some example usages:

```bash
# simplest example
youtube-dl https://www.youtube.com/watch?v=Zuwa8zlfXSY

# customize the filename of the output
youtube-dl -o '%(title)s by %(uploader)s.%(ext)s' https://www.youtube.com/watch?v=Zuwa8zlfXSY

# download from multiple urls
youtube-dl <url1> <url2>

# or use a file with list of urls
youtube-dl -a url.txt

```
If you are more interested, there are plenty of other options to be explored from [documentation page.](https://github.com/ytdl-org/youtube-dl)

## Shutting down the machine
- `shutdown -h now`
-If you want to Shutdown the system and turn the power off immediately.
- `shutdown -h +10`
-If you want to Shutdown the system after 10 minutes.
- `shutdown -r now`
-If you want to Reboot the system using shutdown command.


## Moving between Directories
- Exploring `cd`(change directory) command

-`cd [directory_name]`\
-If you want to change directory to a particular directory,use this command. Eg: cd Documents

-`cd dir/subdir/subsubdir`\
-If you want to move inside a directory from a directory,use this command. Eg: cd Documents/Hacktoberfest/linuxCommands

-`cd /`\
-If you want to change directory to the root directory. Root directory is the first directory in your file system hierarchy.

-`cd ~` or `cd`\
-If you want to change directory to the home directory.Generally known as $HOME,located at path /home/<your username>/.
  Also, `cd` command can be used to do the same above operation.

-`cd ..`\
-It is used to go one level back directory(i.e to parent directory of current directory).

-`cd ../..`\
-It is used to go two levels back directory(i.e to parent's parent directory of current directory).

-`cd -`\
-It is used to change back to the previous working directory. Eg: If `Documents` is present working directory and `Downloads` is previous working directory, this command takes you back to `Downloads` directory.

-`cd "dir name"` or `cd dir\ name`\
-This command is used to navigate to a directory with white spaces.Instead of using double quotes we can use single quotes then also this command will work.Eg: `cd "linux commands"` or `cd linux\ commands` will move to 'linux commands' directory.
##configure to mysql
- 'mysql -u root -p'
-enter the mysql password

## Creating and Removing Directories
* `mkdir` command is used for creating directories.
  - Creating a directory is pretty straightforward.  
        `mkdir [dir-name]`  
    
   - Creating a complete directory structure. (Non of the directories should already exist)   
         `mkdir -p dir1/dir2/dir3`
   - Make `mkdir` emmit the details of operation.    
          `mkdir -v [dir-name]`
          
* `rmdir` command is used for removing empty directories.
  - Removing a directory is also pretty straightforward.  
        `rmdir [dir-name]`  
    
   - Make `rmdir` ignore non empty directories.  
        BY default, the rmdir command throws an error if you try deleting a non-empty directory. However, if you want, you can suppress this behavior of rmdir using the `--ignore-fail-on-non-empty` option.
        
         `rmdir --ignore-fail-on-non-empty [dir-name]`
   - Remove parent directories along with the directory.    
          `rmdir -p test/test-dir/`
        
* `rm -r` command is used for removing non empty directories.
  - Removing a non empty directory is also pretty straightforward.  
        `rm -r [dir-name]`  
        This will present a prompt for approval to delete each of the files. 
        
  - If you don't want such a prompt,  
        `rm -rf [dir-name]`  
        This will not present a prompt for approval to delete each of the files.

## Compress files on linux

The following commands are used to compress files on linux. There are many ways to compress files in linux, the most common is **tar**

* tar
  - The following commands makes an archive named archive.tar containing file foo and bar present in the current directory.
  - ```tar -cf archive.tar foo bar```
  - This command lists all the files in an archive verbosely.
  - ```tar -tvf archive.tar```
  - The `tar` utility has many options which can be seen using
  - ```tar --help```

  ## Basic Commands

    ### `wc`

    - One of the most basic commands, `wc` allows the user to count the number of bytes, characters, words and lines of each given file or standard input and print the result.

    - ***Basic Use:***

    Syntax:
    ```bash
    $ wc filename  # output: number_of_lines number_of_words number_of_characters /path/to/file
    ```

    Example:
    ```bash
    $ wc /proc/cpuinfo  # output: 208 1232 6336 /proc/cpuinfo
    ```

    ### `touch`

    - `touch` is a simple command that allows the user to create an empty file. Note that with `touch`, you can only create the file and not edit it.

    - ***Basic Use:***

    Syntax:
    ```bash
    $ touch filename
    $ ls -l filename
    -rw-rw-rw- 1 current_user users 0 Oct  9 22:03 filename
    ```

    Example:
    Logged in as user ***linux_is_awesome***
    ```bash
   $ touch hello
   $ ls -l hello
   -rw-rw-rw- 1 linux_is_awesome users 0 Oct  9 22:03 hello
    ```

    ### `whoami`

    - `whoami` command displays the username of the current user.

    - ***Basic Use:***

    Syntax:
    ```bash
    $ whoami
    current_user
    ```

    Example:
    Logged in as user ***linux_is_awesome***
    ```bash
   $ whoami
   linux_is_awesome
    ```

### `grep`
- `grep` is an extremely useful command to know in Linux.
- It stands for “global regular expression print". Basically, it's used for pattern matching. `grep` processes text line by line and prints any lines which match a specified pattern.

- ***Basic Use:***
Syntax:
```bash
$ grep [option(s)] pattern [file(s)]
 ``` Creating a test file for using `grep`:
 ```bash
$  cat > grep_test.txt
This is a test file. AAA, BBB, 123, CaSe ExAmPle.
    ```

Example:
```bash
$ grep AAA grep_test.txt
This is a test file. AAA, BBB, 123, CaSe ExAmPle. # AAA will be highlighted in the output

$ grep -i case grep_test.txt  # ignore case while searching
This is a test file. AAA, BBB, 123, CaSe ExAmPle. # CaSe will be highlighted in the output
```
    ###  TO CHECK DISK SPACE USED AND AVAILAVBLE
    - COMMANDS
    $df     (Table that lists for each device name on the system)
    $df -h  (To see output in Human Readable Format)
    $df -m  (Output in one-megabyte)
    $df -k  (Output in one-kilobyte blocks)
    
    ### TO CHECK DISK SPACE USED BY SPECIFIED FILES AND FOR EACH SUB-DIRECTORY
    -COMMANDS
    $du      (Names and space consumption of each of the directories including all subdirectories)
    $du -h   (To see output in Human Readable Format)
    
    To find out /etc/ directory space usage :
    $du /etc/
    $du -h /etc/
    
 
 ### `diff`
- `diff` is an extremely useful command to know in Linux and often used in GIT as well as `git diff`.
- Compare FILES line by line

- ***Basic Use:***
Syntax: diff [OPTION]... FILES
```bash
$  cat > diff_test_file1.txt
This is a test file 1
$  cat > diff_test_file2.txt
This is a test file 2
   ```
Example:
```bash
$ diff diff_test_file1.txt diff_test_file2.txt
1c1
< This is a test file 1
---
> This is a test file 2
```

