<h1 align="center">Linux/Unix Commands</h1>


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


-`ls -l`\
-Displays long list view with detailed file information including file type, permissions, link count, owner, group, size, date and time

-`ls -lt`\
-Lists all files sorted by date and time with the newest file first.

-`ls -ltr`\
-Lists all files sorted by date and time with the oldest file first.

-`ls -lh`\
-Displays all files in current directory with file sizes in human readable format(eg:1.6K,328M,2.4G)

-`ls -a`\
-If you want to list all files including hidden files that start with "."

-`ls -la`\
-Lists all files,including hidden files,in the current directory with detailed information.

-`ls -F`\
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

## Compress files on linux

The following commands are used to compress files on linux. There are many ways to compress files in linux, the most common is **tar**

* tar
  - The following commands makes an archive named archive.tar containing file foo and bar present in the current directory.
  - ```tar -cf archive.tar foo bar```
  - This command lists all the files in an archive verbosely.
  - ```tar -tvf archive.tar```
  - The `tar` utility has many options which can be seen using
  - ```tar --help```
  

