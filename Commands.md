<h1 align="center">Linux/Unix Commands</h1>

## Listing Files
-`ls`\
-If you want to see the list of files on your UNIX or Linux system, use the `ls` command

## Listing Hidden Files and Normal Files
- `ls -al`
-If you want ot see the list of all files with all hidden files in the Current directory system in Linux 

## Creating & Viewing Files
-To create a new file, use the command\
1.`cat > filename`\
2.Add content\
3.Press `ctrl + d` to return to command prompt.\
-To view a file, use the command\
`cat filename`

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
-`su -`\
-`sudo -i`\
-These commands will ask you for password.
2. To jump right into root, run\
-`sudo su -`\
-Since there is no root password made after live install.
3. To run other commands as root temporarily, use the command\
-`sudo` *`command`*\
-Replace the *command* above with your command. Eg: `sudo apt-get update`

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

