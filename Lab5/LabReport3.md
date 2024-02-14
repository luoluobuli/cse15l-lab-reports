## Lab Report 3
### Part 1 - Bugs
The bug I chose is from the method reverseInPlace() in ArrayExamples.
```
public class ArrayExamples {
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
1. A failure-inducing input for the buggy program, as a JUnit test and any associated code
   ```
   @Test
   public void testReverseInPlace() {
     int[] input1 = {1, 2, 3, 4, 5};
     ArrayExamples.reverseInPlace(input1);
     assertArrayEquals(new int[]{5, 4, 3, 2, 1}, input1);
   }
   ```
2. An input that doesn't induce a failure, as a JUnit test and any associated code
   ```
   @Test
   public void testReverseInPlace() {
     int[] input2 = {1};
     ArrayExamples.reverseInPlace(input2);
     assertArrayEquals(new int[]{1}, inpu2);
   }
   ```
3. The symptom, as the output of running the tests
   ![Image](Screenshot.png)
4. The bug, as the before-and-after code change required to fix it
   Before:
   ```
   static void reverseInPlace(int[] arr) {
     for(int i = 0; i < arr.length; i += 1) {
       arr[i] = arr[arr.length - i - 1];
     }
   }
   ```
   After:
   ```
   static void reverseInPlace(int[] arr) {
     int[] temArray = new int[arr.length];
     for(int i = 0; i < arr.length; i += 1) {
       temArray[i] = arr[arr.length - i - 1];
     }
     for(int i = 0; i < arr.length; i += 1) {
       arr[i] = temArray[i];
     }
   }
   ```
