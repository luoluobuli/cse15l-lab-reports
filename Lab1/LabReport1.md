# Lab Report 1
## Examples of using `cd`
### With no arguments
```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
- Working directory: home
- I didn't get any output because I didn't specify my destination directory after my command, thus I didn't move and still stay in the current directory.
- No error

### With a path to a directory as an argument
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
- Working directory: home
- No output pops out, because the `cd` command doesn't return an output if it is executed successfully. But in the command line I can see the working directory was switched to lecture1.
- No error

### With a path to a file as an argument
```
[user@sahara ~/lecture1]$ cd en-us.txt
bash: cd: en-us.txt: No such file or directory
[user@sahara ~/lecture1]$ 
```
- Working directory: lecture1
- The ouput says the the file is not found, because the file I was looking for is not in the current directory lecture1. Instead, it's in the message directory.
- It is an error because the output shows that the command was not successfully executed.

## Examples of using `ls`
### With no arguments
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
[user@sahara ~/lecture1]$ 
```
- Working directory: lecture1
- The output prints names of all files and directories in the current directory
- No error

### With a path to a directory as an argument
```
[user@sahara ~/lecture1]$ ls ..
lecture1
[user@sahara ~/lecture1]$ 
```
- Working directory: lecture1
- The output prints lecture1, because the argument `..` leads to the working directory's parent directory, which is the home directory, and lecture1 is the only thing exists in the home directory.
- No error

### With a path to a file as an argument
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
[user@sahara ~/lecture1]$
```
- Working directory: lecture1
- The output prints the filename I put in as the argument, since when the argument is a file, there couldn't be any file or directory inside it, so the computer just returns the filename itself.
- No error

## Examples of using `cat`
### With no arguments
```
[user@sahara ~/lecture1]$ cat
hello
hello
helloworld
helloworld
^C
[user@sahara ~/lecture1]$
```
- Working directory: lecture1
- When I executed `cat` without arguments, there was no output showing up, neither did the new command line with $. When I typed in a string and pressed enter, it repeated my input. After I pressed ctrl C, the program ended. It is because without any file arguments, `cat` doesn't have any files to read from, so it starts reading from my keyboard as input.
- No error

### With a path to a directory as an argument
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory
[user@sahara ~/lecture1]$
```
- Working directory: lecture1
- The output says messages is a directory and didn't prints any content inside it. It is because `cat` only reads and displays the content inside files. If the user wants to look at what a directory contains, they should use `ls` instead.
- It is an error because we can't put a file as an argument of `cat`

### With a path to a file as an argument
```
[user@sahara ~/lecture1]$ cat messages/ja.txt
こんにちは世界
[user@sahara ~/lecture1]$
```
- Working directory: lecture1
- The output prints the content inside the file ja.txt, because `cat` reads and displays the content inside files.
- No error
