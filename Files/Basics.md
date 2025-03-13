## SWIFT TESTING

### BASICS

- We need to:

```
import Testing
@testable import - here you import your project which will be tested
```

To start writing the first test we need to use @Test attribute:

```
@Test func test() {
  // Write here your test
}
```
![1](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/1.png)

To check conditions we use **#expect** macro

![2](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/2.png)

![3](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/3.png)

![4](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/4.png)

### When you want to stop earlier when the expectation fails we can use **#require** macro

![5](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/5.png)

![6](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/6.png)

Another way to use **#required** macro is to unwrap the optional value

![7](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/7.png)

To add a custom display name we can add a description for the @Test: 

![8](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/8.png)

## TRAITS

![9](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/9.png)

### TRAITS TYPES

![10](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/10.png)

### WRAPPING TESTS

![11](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/11.png)

### SUITE

![12](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/12.png)

## COMMON WORKFLOWS

![13](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/13.png)

### TESTS WITH CONDITIONS

![14](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/14.png)

![15](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/15.png)

![16](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/16.png)

![17](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/17.png)
``` When the entire body of a test can only run on certain OS versions, you can place the @available(...) attribute on that test to control which versions it will run on. Use the @available(...) attribute rather than checking at runtime using #available. The @available(...) attribute allows the testing library to know that a test has an OS version condition, so this can be reflected in the results more accurately. ```

### TESTS WITH COMMON CHARACTERISTICS

![18](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/18.png)

![19](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/19.png)

### GROUPING UNDER SUBSUITE

![20](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/20.png)

![21](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/21.png)

![22](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/22.png)

![23](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/23.png)

![24](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/24.png)

### TESTS WITH DIFFERENT ARGUMENTS

![25](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/25.png)

### PARAMETERIZED TESTING

![26](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/26.png)

![27](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/27.png)

![28](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/28.png)

![29](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/29.png)

## SWIFT TESTING AND XCTEST COMPARISON

![30](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/30.png)

![31](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/31.png)

![32](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/32.png)

![33](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/33.png)

![34](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/34.png)

![35](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/35.png)

![36](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/36.png)

![37](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/37.png)

![38](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/38.png)

### SWIFT TESTING COMMAND LINE EXPERIENCE

![39](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Images/39.png)

[< BACK](https://github.com/ceboolion/SwiftTesting)
