# Software Practices:
Here are other usefull software practices - 
* **Testing:** Testing your code is essential before deployment. It helps you catch errors and faulty conclusions before they make any major impact
* Logging
* Code reviews



## Useful Terms:

* **TEST DRIVEN DEVELOPMENT:** a development process where you write tests for tasks before you even write the code to implement those tasks.
* **UNIT TEST:** a type of test that covers a “unit” of code, usually a single function, independently from the rest of the program.We want to test our functions in a way that is repeatable and automated. Ideally, we'd run a test program that runs all our unit tests and cleanly lets us know which ones failed and which ones succeeded.
* **Unit Test Advantages and Disadvantages:**
The advantage of unit tests is that they are isolated from the rest of your program, and thus, no dependencies are involved. They don't require access to databases, APIs, or other external sources of information. However, passing unit tests isn’t always enough to prove that our program is working successfully. To show that all the parts of our program work with each other properly, communicating and transferring data between them correctly, we use integration tests.

* **Pytest:** This is python unit testing tool. In the test output, periods represent successful unit tests and F's represent failed unit tests. Since all you see is what test functions failed, it's wise to have only one assert statement per test. Otherwise, you wouldn't know exactly how many tests failed, and which tests failed. Starting guide -
  > Create a test file starting with `test_`.
  > Define unit test functions that start with test_ inside the test file.
  > Enter pytest into your terminal in the directory of your test file and it will detect these tests for you!

