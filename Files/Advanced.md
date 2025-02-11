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

```
Any sendable collection, including arrays, dictionaries, ranges, and more can be passed to the test attribute.
```
![22](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/22.jpg)

### PARAMETRIZED TEST WITH 2 ARGUMENTS
```
Test functions in Swift Testing can accept multiple inputs,
and you can add another argument to this test by simply appending it after the first argument.
```
![23](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/23.jpg)

![24](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/24.jpg)

```
To help control this exponential growth, test functions accept a maximum of two collections.
We can also use the Swift standard library's zip function to match up pairs of inputs that should go together.
```
![25](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/25.jpg)

## ORGANIZING TESTS
For basic organization check [Swift Testing Basics](https://github.com/ceboolion/SwiftTesting/tree/main/Files/Basics.md)

```
By adding sub suites, you can reflect this organization in the tests themselves,
and make relationships between these groups of tests, more obvious.
```
![26](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/26.jpg)

```
Tags are another trait that help you organize your tests.
A complex package or project may contain hundreds or thousands of tests and suites.
```
![27](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/27.jpg)

```
Multiple TAGS
```
![28](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/28.jpg)

```
Searching by the TAG
```
![29](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/29.jpg)

```
See all tags
```
![30](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/30.jpg)

## TESTING IN PARALLEL
```
Parallel testing is enabled by default in Swift Testing,
so you can start taking advantage of these features with no extra code.
For the first time, you can run parallel tests on all physical devices,
bringing all these great advantages to even more tests!
```

```
Tests run one after another in serial testing.
If you've used XCTest before, this is how it runs tests by default.

This is in contrast to parallel testing, where tests execute concurrently.
You gain several advantages when your tests run in parallel.
```
![31](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/31.jpg)

```
First, execution time will be reduced, which is crucial in CI where every minute counts.
This also means a faster turnaround to get your results.
Swift Testing runs test functions in parallel by default, regardless of whether they are synchronous or asynchronous.
This is a notable difference from XCTest, which only supports parallelization using multiple processes,
each running one test at a time.
```

```
Let's look at an example. I have two tests: in the first one, I bake a cupcake, and in the second one I eat it.

If these tests always run in order and run one after the other,
then I'll always have a cupcake ready for the second test because it was baked in the first test. That wasn't intentional!
If the tests run in parallel, then the second test's dependency on the first will be exposed at runtime and I'll be able to fix it.
```
![32](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/32.jpg)

### RUNNING TESTS SERIALLY
![33](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/33.jpg)
```
These tests will lose the advantages of being parallel,
so you should first consider refactoring your test code,
whenever possible, to run in parallel.
```

### ASYNCHROMOUS CONDITIONS
```
When writing concurrent test code,
you can use the same concurrency features in Swift as you would in your production code.
```
![34](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/34.jpg)

```
Some code, especially older code written in C or Objective-C,
uses completion handlers to signal the end of an asynchronous operation.
This code will run after the test function returns,
and you won't be able to verify the function succeeded.
```
![35](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/35.jpg)

```
If the code you're testing uses a completion handler and an async overload is NOT available,
you can instead use withCheckedContinuation or withCheckedThrowingContinuation
to convert it to an expression that can be awaited.
```
![36](https://github.com/ceboolion/SwiftTesting/blob/main/Files/ImagesAdvanced/36.jpg)

[< BACK](https://github.com/ceboolion/SwiftTesting)
