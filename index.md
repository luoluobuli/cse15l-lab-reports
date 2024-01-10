hello world!
*test*
**test**
# test
## test
[CSE 15L week 1 course page] (https://ucsd-cse15l-w24.github.io/week1/index.html)
![Power] (https://upload.wikimedia.org/wikipedia/en/c/c2/Power_%28Chainsaw_Man%29.png)
> test

* test1
* test2
* test3

1. test1
2. test2
3. test3

---

type `javac Hello.java` in the terminal

Hello.java:
```
public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}
```
