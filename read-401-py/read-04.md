# Classes and Objects

  * Objects get their variables and functions from classes.
  * Classes are essentially a template to create your objects.

  * Accessing Object Variables
  ```
  class MyClass:
      variable = "blah"
  
      def function(self):
          print("This is a message inside the class.")

  myobjectx = MyClass()
  
  myobjectx.variable
  ```

   ***Accessing Object Variables:***

   we can di it using myobjectx.variable

   ***Accessing Object Functions:***

   we can do it using myobjectx.function()


   ## Thinking recursively in python
   
   If the current problem represents a simple case, solve it. If not, divide it into subproblems and apply the same strategy to them.

   in python, a recursive function is a function that calls itself and repeats its behavior until some conditions are met to return a result all recursive functions share the same structure, a base case, and a recursive case

   Recursive function for calculating n! implemented in Python:
   ```
    def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
   ```

   ## Python Testing with pytest: Fixtures and Coverage

   Pytest is a robust Python testing tool, pytest can be used for all types and levels of software testing. pytest can be used by development teams, QA teams, independent testing groups, individuals practicing TDD, and open source projects. In fact, projects all over the Internet have switched from unittest or nose to pytest, including Mozilla and Dropbox. Why? Because pytest offers powerful features such as ‘assert‘ rewriting, a third-party plugin model, and a powerful yet simple fixture model that is unmatched in any other testing framework.

   ## pytest fixtures

   1. capfd: Capture, as text, output to file descriptors 1 and 2.

   1. capfdbinary: Capture, as bytes, output to file descriptors 1 and 2.

   1. caplog: Control logging and access log entries.

   1. capsys: Capture, as text, output to sys.stdout and sys.stderr.

   1. capsysbinary: Capture, as bytes, output to sys.stdout and sys.stderr.

   1. cache: Store and retrieve values across pytest runs.

   1. doctest_namespace: Provide a dict injected into the docstests namespace.

   1. monkeypatch: Temporarily modify classes, functions, dictionaries, os.environ, and other objects.

   1. pytestconfig: Access to configuration values, pluginmanager and plugin hooks.

   1. record_property: Add extra properties to the test.

   1. record_testsuite_property: Add extra properties to the test suite.

   1. recwarn: Record warnings emitted by test functions.

   1. request: Provide information on the executing test function.

   1. testdir: Provide a temporary test directory to aid in running, and testing, pytest plugins.

   1. tmp_path: Provide a pathlib.Path object to a temporary directory which is unique to each test function.

   1. tmp_path_factory: Make session-scoped temporary directories and return pathlib.Path objects.

   1. tmpdir: Provide a py.path.local object to a temporary directory which is unique to each test function; replaced by tmp_path.

   1. tmpdir_factory: Make session-scoped temporary directories and return py.path.local objects; replaced by tmp_path_factory.

Done
---
 
[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)