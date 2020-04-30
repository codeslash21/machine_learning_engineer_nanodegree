# Software Practices:
Here are other usefull software practices - 
* **Testing:** Testing your code is essential before deployment. It helps you catch errors and faulty conclusions before they make any major impact
* **Logging:** Logging is valuable for understanding the events that occur while running your program. For example, if you run your model over night and see that it's producing ridiculous results the next day, log messages can really help you understand more about the context in which this occurred.
* **Code reviews:** Code reviews benefit everyone in a team to promote best programming practices and prepare code for production. Some benefits are -
  * Catch errors.
  * Ensure readablity
  * Check standards are met.
  * Share knowledge among teams.
  
During code reviews we have to check the followings -
  - Is the code clean and modular?
    - Can I understand the code easily?
    - Does it use meaningful names and whitespace?
    - Is there duplicated code?
    - Can you provide another layer of abstraction?
    - Is each function and module necessary?
    - Is each function or module too long?
  - Is the code efficient?
    - Are there loops or other steps we can vectorize?
    - Can we use better data structures to optimize any steps?
    - Can we shorten the number of calculations needed for any steps?
    - Can we use generators or multiprocessing to optimize any steps?
  - Is documentation effective?
    - Are in-line comments concise and meaningful?
    - Is there complex code that's missing documentation?
    - Do function use effective docstrings?
    - Is the necessary project documentation provided?
  - Is the code well tested?
    - Does the code high test coverage?
    - Do tests check for interesting cases?
    - Are the tests readable?
    - Can the tests be made more efficient?
  - Is the logging effective?
    - Are log messages clear, concise, and professional?
    - Do they include all relevant and useful information?
    - Do they use the appropriate logging level?

[Python Code linter](https://www.pylint.org/) - This can be used for code reviews to save time.

## Useful Terms:

* **TEST DRIVEN DEVELOPMENT:** a development process where you write tests for tasks before you even write the code to implement those tasks.
* **UNIT TEST:** a type of test that covers a “unit” of code, usually a single function, independently from the rest of the program.We want to test our functions in a way that is repeatable and automated. Ideally, we'd run a test program that runs all our unit tests and cleanly lets us know which ones failed and which ones succeeded.
* **Unit Test Advantages and Disadvantages:**
The advantage of unit tests is that they are isolated from the rest of your program, and thus, no dependencies are involved. They don't require access to databases, APIs, or other external sources of information. However, passing unit tests isn’t always enough to prove that our program is working successfully. To show that all the parts of our program work with each other properly, communicating and transferring data between them correctly, we use integration tests.

* **Pytest:** This is python unit testing tool. In the test output, periods represent successful unit tests and F's represent failed unit tests. Since all you see is what test functions failed, it's wise to have only one assert statement per test. Otherwise, you wouldn't know exactly how many tests failed, and which tests failed. Starting guide -
  * Create a test file starting with `test_`.
  * Define unit test functions that start with test_ inside the test file.
  * Enter pytest into your terminal in the directory of your test file and it will detect these tests for you!
  
* **Log messages:** Some useful tips for log messages -
  - Be professional and clear
  - Be concise and use normal capitalization
  - Choose the appropriate level for logging
  ```
  DEBUG - level you would use for anything that happens in the program.
  ERROR - level to record any error that occurs
  INFO - level to record all actions that are user-driven or system specific, such as regularly scheduled operations
  ```
  - Provide any useful information
  
  Some examples of log messages -
  ```
  Bad: Failed to read location data
  Good: Generating product recommendations.
  Bad: Hmmm... this isn't working???
  ```

