#Code Review 

####Code Compiles

Compilation of a source code is absolutely mandatory. A developer does not need to review the source code that does not compile.  
* The first pre-requisite before you even think about starting code review.
* Making sure all major compiler warnings are removed.

####Unit Tests

A developer must have unit tests for all code changes. Its a peer code review best practice to also review unit tests and ensure all scenarios are covered. 
* Must have pre-requisite for starting code review.
* Use code coverage tools to ensure completeness of tests.

####Code Is Functional

A peer code reviewer need to ensure the code is functional and performs the expected job. This may involve sitting with the developer and doing a test run and observing results.

####Code Is Unit Testable

A peer code reviewer need to ensure the code has sufficient and required unit tests. Sometimes this may be difficult since the code is not unit testable. Necessary code refactoring need to performed to ensure code can be unit tested.

####Code Is Easy To Debug

A peer code reviewer need to ensure the code is easy to debug in non developer environment. This may relate to few things 
* There needs to be enough logging in the code. Code needs provide enough logging to work in debugging mode for application.
* There needs to be enough comments in the code.
* There needs to be enough monitoring related code.

####Code Documentation

Writing code comments is helpful however not always necessary. Sometimes the code is not self explanatory, or does something un-usual. It needs to be well documented.

####Code Indentation And Readability

All developers in a team needs to use common formatting tool with same formatting styles to avoid version control conflicts and difficulty in reading file changes. There is no right or wrong way to format code, however make sure the team uses the same formatting.

####Exception Handling

Exception handling code is often ignored in critical timelines. A code reviewer must ensure that sufficient exception handling is done in code. Unit test cases should also be addd to check for all exception scenarios. Some common exception scenarios are
* Null objects
* Empty objects
* Invalid format values
* Boundary conditions

####Logging Key Attributes For Debugging

Debugging information is important to support and maintain applications. Logging required key attributes makes the job of dev ops and support team easy. Developer and Code reviewer needs to ensure that all key attributes are being logged.

####Eliminate Unwanted Code And Libraries If Not Used

Its common habit of developers to not remove unused code from a file. This is mainly since they think it may be required in future. Some developers tend to comment it so it can be used later. This makes the code unreadable. The code reviewer must make sure that all such code is removed. Developers can always go back to a previous version of code in version control. However, in my observation, a commented code is almost always not reused.

####Handling NULL And Empty Object Scenarios

Not handling NULL and Empty objects causes many production related problems. A code reviewer must be explicitly watching for these issues.  Unit test cases should also be addd to check for all NULL and Empty object scenarios.

####Sticking To Coding Standards

Stick to [the standard coding practices](./style-guide.md) to ensure everyone speaks the same language. It makes it easier for a new developer to start understanding the code faster.

####Avoid Hard Coding - Prefer Configuration

Many configurations are often hard coded by developers inside the compiled code and makes it difficult to change the behavior of software. For example an optional feature should have a configuration that can enable or disable a feature. I code reviewer my look for such opportunities to ensure configuration is preferred over hard coding.

####Code Performance

Performance of the code is important, however difficult to measure depending on type of software. Its important that a code reviewer looks at the performance of a code in various aspects. 
* Time to do the task - How much time it take to finish the task. Is it acceptable?
* Memory or Number of objects used to do the task.  Is it acceptable?
* Number of threads or processes to do the task.  Is it acceptable?
* Concurrency limits of the task. How many tasks can be performed by the program concurrently

####Scalability

Scalability of the code may be a important concern, depending on your requirements.  Its important that a code reviewer looks at the scalability of a code in various aspects. 
* Will the current software scale with new changes.
* Will there be any impact on scalability in future.

####Code Security Review

This is most difficult step in code review since not many people know how to write secure code. Some common guidelines are listed below for a secure code
* Encrypt sensitive user information (e.g. SSN, passwords, credit card numbers etc)
* Never log sensitive information on log files, it can be dangerous and make hacking easy.
* Disable Weak Ciphers on your app/web servers.
* Use trusted libraries for cryptography and encryption instead of inventing your own.
* Watch for OWASP top 10 issues are addressed in a web facing application.

####Releasing Resources

Releasing resources in a busy application is really important step that is often missed out by hasty developers. Ensure all important and shared resources are being released by each code block. Following scenario must be covered

* Releasing of resources after the task is completed successfully.
* Releasing resources after the task has failed.
* Release resources after there is exception in processing task.

####Encourage Code Reusability

Copy/Paste is developers best friend.  Many lines of code is duplicated by simply doing a copy paste. This seems to solve problem in short term however creates maintenance issues in long run. Any copy/paste candidate in code must be refactored to be re-usable. It needs to be done carefully since many other code blocks may be calling it already.

####Concurrency, Thread Safety And Deadlock Related Issues Are Considered

Most of the developers are not writing multi threading code and concurrent applications. Therefore these aspects are often ignored by developers. You must pay careful attention to your code block and understand its behavior when multiple thread will try to access it at same time. Ensure all shared variables are minimized and handling concurrency of multiple threads is not leading to a potential deadlock situation.

####Use Of Design Patterns When Required

It is not easy to spot a design pattern in a bad code, however an experience programmer can easily suggest a better approach provided enough knowledge of the software. 
Try to spot common design pattern application on existing code and see how you can improve it. Use of design pattern improves maintainability of source code.
