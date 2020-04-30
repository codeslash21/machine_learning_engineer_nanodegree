# Software Engineering Practices:

Best software engineering practices are follows - 
* Writing clean and modular code
* Writing efficient code
* Code refactoring
* Adding meaningful documentation
* Using version control

## Some Important Terms:

* **PRODUCTION CODE:** software running on production servers to handle live users and data of the intended audience. Note this is different from production quality code, which describes code that meets expectations in reliability, efficiency, etc., for production. Ideally, all code in production meets these expectations, but this is not always the case.
* **CLEAN:** readable, simple, and concise. A characteristic of production quality code that is crucial for collaboration and maintainability in software development.
* **MODULAR:** logically broken up into functions and modules. Also an important characteristic of production quality code that makes your code more organized, efficient, and reusable. Making your code modular make it easier to -
  - Reuse your code.
  - Write less code.
  - Read your code.
  - Collaborate on your code.
* **MODULE:** a file. Modules allow code to be reused by encapsulating them into files that can be imported into other files.

* **REFACTORING:** restructuring your code to improve its internal structure, without changing its external functionality. This gives you a chance to clean and modularize your program after you've got it working.
  * Reduce workload in long run.
  * Easier to maintain code.
  * Reuse more of your code.
  
* **Clean Code:** Write clean code means -
  - Using meaningful names
  > Be descriptive and imply type
  > Be consistent but clearly differentiate
  > Avoid abbreviations and especially single letters - (Exception: counters and common math variables)
  > Long names != descriptive names
  
  - Nice whitespace
  > Try to limit your lines to around 79 characters, which is the guideline given in the PEP 8 style guide
  
* **Modular Code:** Following thingss to remember -
  * DRY (Don't Repeat Yourself)
  * Abstract out logic to improve readability
  * Minimize the number of entities (functions, classes, modules, etc.)
  * Functions should do one thing
  * Arbitrary variable names can be more effective in certain functions
  * Try to use fewer than three arguments per function
  
* **Efficient Code:**
Knowing how to write code that runs efficiently is another essential skill in software development. Optimizing code to be more efficient can mean making it:
  * Execute faster
  * Take up less space in memory/storage
  
* **DOCUMENTATION:** additional text or illustrated information that comes with or is embedded in the code of software.
Helpful for clarifying complex parts of code, making your code easier to navigate, and quickly conveying how and why different components of your program are used.
Several types of documentation can be added at different levels of your program:
  * **In-line Comments - line level:** In-line comments are text following hash symbols throughout your code. They are used to explain parts of your code, and really help future contributors understand your work.
  * **Docstrings - module and function level:** Docstring, or documentation strings, are valuable pieces of documentation that explain the functionality of any function or module in your code. Ideally, each of your functions should always have a docstring.
  * **Project Documentation - project level:** Project documentation is essential for getting others to understand why and how your code is relevant to them, whether they are potentials users of your project or developers who may contribute to your code. A great first step in project documentation is your README file. It will often be the first interaction most users will have with your project.
  
  
  
