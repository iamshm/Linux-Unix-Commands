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

## Get root access
1. To log in as a super user, run one of the following commands. You can actually use this command to log in as any user on the machine, but when left blank it will attempt to log in as root.\
-`su -`\
-`sudo -i`\
-These commands will ask you for password.
2. To jump right into root, try running\
-`sudo su -`\
-Since there is no root password made after live install.
3. To run other commands as root temporarily, use the command\
-`sudo` *`command`*\
-Replace the *command* above with your own command. Eg: `sudo apt-get update`


