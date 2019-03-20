# Test Driven Development
Test driven development is a useful skill in the Software Development Life Cycle (SDLC), which allows developers to check the quality of a solution

## Structure of Tests
Testing in software projects is often implemented using a few key concepts:
	* Test Case: The smallest atomic unit in the testing process. Test a single scenario/case of a given feature. E.g. assert order.calculateCost() = 50, where the sum of all order items is $50
	* Test Suite: A group of test cases or other test suites which, combined, test a subset of related features
	* Test runners: control the execution and outcomes of tests
	* Test fixtures: Methods which are run as part of executing test. E.g setup or compeltion methods which run before and after each test respectively

## Deriving tests from AC
When AC are well written (i.e have clear actions and outcomes), they can be easily turned into test cases. Note, the following relationships are not precise, and may vary slightly for more/less complex systems
	* User Stories (describing single features) may become test suites
	* Each AC for a user story may become one or more test cases for these test suites
	* Epics may also become test suites which consist of smaller test suites for each of its features (User Stories)

## Tests in (Python) Code
Fue to the use of the pytest module and the unittest.TestCase class, it is common to write tests in the following manner
	* For each feature (often for each method/function of another class or module), create a class called TestModuleName. These then act like a small test suite for a particular feature or method
	* For each case you want to test, make a method of the Test class which contains an assert statement
	* Once several of these TestMethodName classes have been made, they form a larger test suite.
