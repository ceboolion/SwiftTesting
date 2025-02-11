[SWIFT TESTING BASICS](https://github.com/ceboolion/SwiftTesting/blob/main/Files/Basics.md)

![1](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/1.jpg)

## EXPECTATIONS
![2](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/2.jpg)
![3](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/3.jpg)

### EXPECT THROWS
```
Default ERROR
```
![4](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/4.jpg)

```
Particular type of ERROR
```
![5](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/5.jpg)

```
Specific type of ERROR
```
![6](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/6.jpg)

```
Customized validation of type of ERROR
```
![7](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/7.jpg)

```
Reminder - #required macro
- When we use try #require and it will fail, #expect macro won't be called
```
![8](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/8.jpg)

## HANDLING KNOWN ISSUES
 
```
WHen we are waiting for known issue to be fixed we can use withKnownIssue instead of @Test(.disabled).
Task will be run and we will be notfied about compilation errors - it won't be count as a failure - it will end up as a Expected failure
```
![9](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/9.jpg)

### MULTIPLE CHECKS
```
When our test consists of many checks, we can use withKnownIssue for some of them.
This allows us to run the test without failures and fix other bugs later while compiling all tests successfully.
```
![10](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/10.jpg)

### CUSTOM TEST DESCRIPTIONS
```
Complex types like structures and classes can produce a lot more noise because their descriptions,
by default, include a lot of extra data that may not be useful during testing.
```
![11](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/11.jpg)
![12](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/12.jpg)
```
These values show up in Xcode with a lot of information.
The information is accurate, but it can be hard to find the important bits that distinguish one value from another.
In this case, you may want to give each one a concise test description without affecting production code.

You can make your type conform to the CustomTestStringConvertible protocol which lets you provide a tailored, test-specific description.
```
![13](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/13.jpg)

```
Result:
```
![14](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/14.jpg)

## PARAMETERIZED TESTING
```
With Swift Testing, you can easily run a single test function with many different arguments.
```
```
Enumeration lists various ice cream flavors and you can check if a particular flavor contains nuts.
The containsNuts property needs test coverage for every case in the enumeration.
```
![15](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/15.jpg)

```
We could write a separate test function for each case in the enumeration, but that's a lot of code.
```
![16](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/16.jpg)

```
Instead, we really only need one or two test functions here.
After all, the logic of the tests is the same except for a single input value.
```
![20](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/20.jpg)
```
We can move the inputs up and pass them to the test attribute instead of iterating over them inside the test function.
```
![21](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/21.jpg)

### HOW PARAMETERIZATION WORKS:
```
These test cases are entirely independent of each other and are able to run in parallel.
This means less time is needed to test them all all than would be needed with a for loop or separate test functions.
```
![18](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/18.jpg)

```
Xcode supports re-running individual test cases of a test function, when the type of input conforms to Codable.
This allows you to retry individual failing test cases without needing to re-run other test cases that have run successfully.
```
![19](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/19.jpg)

[< BACK](https://github.com/ceboolion/SwiftTesting)
