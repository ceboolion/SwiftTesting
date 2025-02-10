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
![1](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/1.png)

To check conditions we use **#expect** macro

![2](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/2.png)

![3](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/3.png)

![4](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/4.png)

### When you want to stop earlier when the expectation fails we can use **#required** macro

![5](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/5.png)

![6](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/6.png)

Another way to use **#required** macro is to unwrap the optional value

![7](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/7.png)

To add a custom display name we can add a description for the @Test: 

![8](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/8.png)

## TRAITS

![9](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/9.png)

### TRAITS TYPES

![10](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/10.png)

### WRAPPING TESTS

![11](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/11.png)

### SUITE

![12](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/12.png)

## COMMON WORKFLOWS

![13](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/13.png)

### TESTS WITH CONDITIONS

![14](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/14.png)

![15](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/15.png)

![16](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/16.png)

![17](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/17.png)

### TESTS WITH COMMON CHARACTERISTICS

![18](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/18.png)

![19](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/19.png)

### GROUPING UNDER SUBSUITE

![20](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/20.png)

![21](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/21.png)

![22](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/22.png)

![23](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/23.png)

![24](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/24.png)

### TESTS WITH DIFFERENT ARGUMENTS

![25](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/25.png)

### PARAMETERIZED TESTING

![26](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/26.png)

![27](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/27.png)

![28](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/28.png)

![29](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/29.png)

## SWIFT TESTING AND XCTEST COMPARISON

![30](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/30.png)

![31](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/31.png)

![32](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/32.png)

![33](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/33.png)

![34](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/34.png)

![35](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/35.png)

![36](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/36.png)

![37](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/37.png)

![38](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/38.png)

### SWIFT TESTING COMMAND LINE EXPERIENCE

![39](https://github.com/ceboolion/SwiftSyllabus/blob/main/SwiftTesting/Images/39.png)
