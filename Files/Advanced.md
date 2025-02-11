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
WHen our test consists of many checks, that we can use for some of them withKnownIssue which allow us to run test without failure and fix other bug later compiling all tests successfuly 
```


[< BACK](https://github.com/ceboolion/SwiftTesting)
