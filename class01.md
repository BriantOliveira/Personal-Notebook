# **Let’s Get Started**

### Why should I write a test?

Testing is something that a lot of engineering teams take very seriously from day one and as result, it's a big part of a work environment and development culture. If you haven't done testing before it's ok, hopefully by the end of this tutorial you will become a wizard when it comes to testing.

Testing your code will save you and your team a lot of time, it will make your development experience much easier and work happier by writing unit tests.  Writing test is one of the best ways to get on board with a larger code base.

### Different types of software testing?

There is two types of testing which are Functional and Non-functional test. A few of the most common functional test are:

* Unit testing, 
* Integration testing
* System testing
* Interface testing, and others.

  A few common Non-functional tests are:

* Performance test

* Stress testing

* Load testing

* Reliability testing, and others.

During this tutorial we will talk about three very important tests.

1. Unit Test.
2. End-to-end Test.
3. Harness Test.

If you want to read more about these other  types tests, I recommend this [article](https://www.softwaretestinghelp.com/types-of-software-testing/).

### What is Unit Testing?

One of the smallest parts of your application is called units, testing these units to check whether is a fit for use or not is called unit testing.

If you are going to create a test  for a given function or component of your code, then we need to make sure that the function or component by itself, separate from everything else, is doing what it is intended to do, no more, not less and mock rest of things which are not under test.

### What is End-to-end Testing?

End-to-end testing involves an application flow from start to end. The purpose of this type of testing methodology is to simulate the real world as in a user scenario in order to validate the system that is under test for data integrity.

The goals is to identify system dependencies and to ensure that the right information is passed between various systems components and system.

It is performed from start to finish under real-world scenarios like communication of the application with hardware, network, database and other applications.

### What is Harness Testing?

Test harness is a methodology that enables the automation of tests. Automation test is a collection of software and test data with the purpose  to test a program unit by running it under varying conditions and monitoring its behavior and outputs.

Test harness executes test, by using a test library and generates a report.

### TDD vs. BDD

TDD \(Test-Driven Development\) is a process for when you write and and run your test. TDD makes it very  possible to have high test coverage. Test coverage refers to the percentage of you code base that is tested automatically, so a higher number is better.

The TDD process consist of the following steps:

1. Start by writing test.
2. Write test against your function or container, testing for edge cases.
3. Write the minimum amount of code to make it pass. 
4. Optionally refactor your code.
5. Repeat all this cycle.

BDD \(Behavior-Driven Development\) is a set practice that aim to reduce  wasteful activities in software development. A good trick to remember how to a BDD is the formula 'Given-When-Then'.

The BDD process consist of the following steps:

1. **Given** a certain scenario
2. **When** an action takes place
3. **Then** this should be the outcome.

A practical example would be:

1. **Given** the User has not entered any data on the form
2. **When** he clicks the submit button
3. **Then** proper validation messages should be shown.



