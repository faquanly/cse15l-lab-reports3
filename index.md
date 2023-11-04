# LAB REPORT 3 - Bugs and Commands
## Emma Nguyen - PID 18021060
1. Part 1 - Bugs
   - Choose one of the bugs from week 4's lab
     
    ```
    ArrayExamples.java
    
    public class ArrayExamples {
    // Changes the input array to be in reversed order
    static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
   }
    // Returns a *new* array with all the elements of the input array in reversed order
   static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
    }
    ```
  
   - A failure-inducing input for the buggy program, as a JUnit test and any associated code.
     ```
     ArrayTests.java
     
     public class ArrayTests {
     @Test
     public void testReverseInPlace() {
     int[] input1 = { 3 };
     ArrayExamples.reverseInPlace(input1);
     assertArrayEquals(new int[]{ 3 }, input1);
     }
     @Test
     public void testReversed() {
      int[] input1 = { };
      assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
      }
     }
	
     ```
     - The failure-inducing inputs are `int[] input1 = { 3 };` in `testReverseInPlace()` and `int[] input1 = { };` in `testReversed()`. When the input with an array of 1 element or no element, the result cannot reflect whether the array is in reversed order or not. Therefore, the code passed the test even though there are bugs in the code.
   - An input that doesn't induce a failure, as a JUnit test and any associated code.
     ```
     int[] input1 = { 1, 2, 3, 4, 5};
     
     ```
     - This input with an array of 5 elements can test if the result is an reversed array or not.
   - The symptom, as the output of running the tests.
   - ![Before: Output of running the test with a failure-inducing input](part1-image1.png)
     - The test is passed eventhougt the code has bug.
   - ![After: Output of running the test WITHOUT a failure-inducing input](part1-image2.png)
     - The code doesn't 
   - The bug, as the before and after code change required to fix it.
   - 
3. Part 2 - Researching Commands
   - I choose the `grep` command.
   - Asking Chat GPT
