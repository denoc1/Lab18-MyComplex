# Lab 18: Complex Numbers

You will be including two files in this lab: `Lab18.java` and `MyComplex.java`.

## Task

Write a class called `MyComplex` which models the complex numbers \(a + bi\).

### Requirements

The `MyComplex` class should contain the following:

- **Instance Variables**
  - Two private `double` variables: `real` and `img`.

- **Constructors**
  - A default constructor to create a complex number at `0 + 0i`.
  - A constructor that takes two `double` values, `a` and `b`, and initializes the complex number to `a + bi`.

- **Accessors (Getters)**
  ```java
  public double getReal()
  public double getImg()

- **String Representation**
     ```java
  public String toString()
     // returns the "a + bi" form of the complex number.
     //If b is negative, the string should be "a - bi".
 

- **Type Checks**
     ```java
  public boolean isReal()
  public boolean isImaginary() 
  //methods to check whether this complex number is real (imaginary part is 0) or   //imaginary (real part is 0), respectively. For example:
  //4 is real
  //5i is imaginary
  //4 + 5i is neither
  //0 is both


- ***Arithmetic Operators on Complex Numbers**
    ```java
  public void add(MyComplex c)
  //Adds complex number c to this complex number. This changes the instance         // variable in front of the dot operator.
  //Note:  (a+bi)+(c+di)=(a+c)+(b+d)i
   ```

 ```java
public void multiply(MyComplex c)
// Multiplies c to this complex number. This also changes the instance variable in //front of the dot operator.
//Note:  (a+bi)∗(c+di)=(ac−bd)+(ad+bc)i
 ```

 ```java
public void conjugate()
//Changes this complex number into its conjugate.
//Hint: The conjugate of a+bi is a - bi
 ```

 ```java
public double argument()
// Returns the argument (angle) in radians of this complex number. This angle is //the same as theta in polar coordinates.
// Hint: Use Math.atan2(b, a).
 ```

 ```java
public double magnitude(): Returns the magnitude or length of this complex number.
//Hint: The magnitude of a+bi is Math.sqrt(a * a + b * b).
//Example: The magnitude of 3 + 4i is 5.
 ```

  -**Static Methods**
  ```java
public static MyComplex addNew(MyComplex a, MyComplex b):
// Returns a complex number that is the sum of a and b. This should not change the //object variables a and b.

public static MyComplex multiplyNew(MyComplex a, MyComplex b):
//Returns the complex number that is the product of a * b. This should not change //the object variables a and b.
 ```


-**Documentation**
  - Use appropriate documentation in your code:
      - Header Comments: Include in MyComplex.java file, including your name, date, any co-authors, and a description of the class.
  ** Method Comments:**
      - Each method must have a documentation statement specifying what the method does.
      - Each method that returns a value (non-void) must include a Post-condition describing what is being returned.
      - Each method that has parameters passed must include a Pre-condition specifying any restrictions on those parameters.
      - Notes
    

Ensure all method headers match the descriptions above. I will test your code using my own Lab18.java file that tests all specified classes (5-13) according to the chart provided. If any of your method code does not run with my test file, you will lose all points for that method
   
   ### Testing Requirement

In addition to implementing `MyComplex.java`, you are required to write a thorough test program in a separate file, `Lab18.java`, to verify that each method in `MyComplex` works correctly. Your test program should include the following:

- **Test all Constructors**: Create several instances of `MyComplex` using different constructors and print them to ensure they are initialized correctly.

- **Test Accessors and Mutators**: For each instance, use the getter methods to verify the real and imaginary parts are correct.

- **Verify String Representation**: Call `toString()` on several `MyComplex` objects with different values (including negative imaginary parts) to confirm that the output matches the expected format.

- **Test Type Check Methods**: Use `isReal()` and `isImaginary()` on various objects and confirm they return the correct boolean values.

- **Validate Arithmetic Operations**: For `add()` and `multiply()`, test the methods with different `MyComplex` values to check if the resulting objects have the expected real and imaginary parts.

- **Test Additional Operations**:
  - For `conjugate()`, verify that each complex number is changed to its conjugate.
  - Use `argument()` and `magnitude()` with known values to confirm that they return accurate results.

- **Static Method Testing**: Use `addNew()` and `multiplyNew()` to create new complex numbers and confirm that the original objects `a` and `b` remain unchanged.

- **Edge Cases**: Include tests for edge cases such as:
  - `0 + 0i`
  - Purely real numbers (e.g., `5 + 0i`)
  - Purely imaginary numbers (e.g., `0 + 5i`)
  - Negative values for real and imaginary parts

Your test program should print descriptive messages that show the method being tested, the inputs, and the expected vs. actual outputs for each test. Aim to make your test cases comprehensive so that every method and possible edge case is covered.   - 
