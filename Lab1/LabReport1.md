# Lab Report 1
## Examples of using `cd`
* with no arguments
```
[user@sahara ~]$ cd
```

* with a path to a directory as an argument
```
[user@sahara ~]$ cd lecture1
```

* with a path to a file as an argument
```
[user@sahara ~/lecture1]$ cd en-us.txt
bash: cd: en-us.txt: No such file or directory
```

## Examples of using `ls`
* with no arguments
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```

* with a path to a directory as an argument
```
[user@sahara ~/lecture1]$ ls ..
lecture1
```

* with a path to a file as an argument
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
```


## Examples of using `cat`
* with no arguments
```
[user@sahara ~/lecture1]$ cat
hello
hello
helloworld
helloworld
```

* with a path to a directory as an argument
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory
```

* with a path to a file as an argument
```
[user@sahara ~/lecture1]$ cat messages/ja.txt
こんにちは世界
```
