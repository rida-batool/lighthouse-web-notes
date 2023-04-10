## Unit Testing

Unit testing is the practice of testing small pieces of code, typically individual functions, alone and isolated. If your test uses some external resource, like the network or a database, it’s not a unit test.

Benefits:

- Should be easy to write, if not easy, your code is bad
- Helps you write better code
- great for preventing regressions – bugs that occur repeatedly. 

## Integration Testing
 The idea is to test how parts of the system work together – the integration of the parts.

 It is same as unit testing but one difference:

 Unit tests are isolated from other components, integration tests are not. 

 Intergration tests are used when you need to test two system at the same time. e.g.  like a database and your app – work together correctly, and that calls for an integration test.

 Prefer unit testing than integration testing as it is hard. Try fixing your code rather than doing inetgration testing unless absolutely necessary.

 ## Functional Testing

Functional testing is also sometimes called E2E testing, or browser testing. They all refer to the same thing.

Functional testing is defined as the testing of complete functionality of some application. In practice with web apps, this means using some tool to automate a browser, which is then used to click around on the pages to test the application.

e.g. Functional testing stimulates real user interactions on web page. so, you should keep functional testing simple and not fine grained as it can be slow. Web page loading time is also a factor to consider.

Read More here: [Types of testing](https://codeutopia.net/blog/2015/04/11/what-are-unit-testing-integration-testing-and-functional-testing/)

## Happy path testing

it is testing most basic and expected flow of event through an application, from the user's perspective.

You test the core functionality of the application that it is working properly, and that the user can complete tasks without encountering any unexpected issues.

However, it is important to note that Happy Path Testing is not sufficient on its own. It is still necessary to test for edge cases, error conditions, and other scenarios that may cause the application to behave unexpectedly.