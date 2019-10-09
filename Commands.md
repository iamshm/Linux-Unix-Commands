<h1 align="center">Linux/Unix Commands</h1>

## listing files
- Frequent forms of `ls` command usage

-`ls`\
-If you want to see the list of files on your UNIX or Linux system, use the `ls` command

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
-To create a new file, use the command\
1.`cat > filename`\
2.Add content\
3.Press `ctrl + d` to return to command prompt.\
-To view a file, use the command\
`cat filename`

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
