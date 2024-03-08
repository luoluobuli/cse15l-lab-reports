### Student's post:
I'm writing the method `removeLast` in `MyDeque` class and it failed the test when I ran my bash script, with error message shown in my screenshot. I also provided the code and script I wrote below. I guess that the rear is not updated correctly, but I couldn't find the bug. How should I fix my code?  
**Error message:**  
![image](error.png)  
**Code:**  
![image](codeNew.png)  
**Test:**  
![image](test.png)  
**Bash script:**  
![image](bash.png)  
**Directory structure:**  
![image](structure.png)

### TA's reply:
You can try use `jdb` to help you find the bug. Use it to check `removeLast` step by step to see what is happening inside the method.  
Here's the commands you can try:
```
$javac -g -cp ".;libs\junit-4.13.2.jar;libs\hamcrest-2.2.jar" CustomTester.java
$jdb -classpath ".;libs\junit-4.13.2.jar;libs\hamcrest-2.2.jar" org.junit.runner.JUnitCore CustomTester
```
Then, set the stop point `stop at CustomTester:30` to look inside your method.  
Type `run`, and then keep doing `step` with `print rear` after each step to keep track of the variable.  
Then you might be able to find the logic mistake in your code.

### Student's update:
