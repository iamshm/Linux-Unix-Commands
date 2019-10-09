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

## Searching for a file
- `find . -name ".js" -print`: find all files with JS extnesion and print them on screen
- `find . -type d -name "*tmp" -print`: print all directories ending with `tmp`
- `find . -type f -exec ls -l {} \;`: use `ls -l` on all returned values

## Exiting the shell
- `exit` (also aliased to `bye` or `quit` in some shell flavors)
