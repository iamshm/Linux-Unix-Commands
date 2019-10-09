<h1 align="center">Linux/Unix Commands</h1>

## listing files
-`ls`\
-If you want to see the list of files on your UNIX or Linux system, use the `ls` command

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

