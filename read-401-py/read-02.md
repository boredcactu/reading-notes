# Python Modules and Packages

## Python Modules:
    
  ---
  There are actually three different ways to define a module in Python:
  
  * A module can be written in Python itself.
  
  * A module can be written in C and loaded dynamically at run-time, like the re (regular expression)        module.
  
  * A built-in module is intrinsically contained in the interpreter, like the itertools module.
  
  ***import Statement***

 Module contents are made available to the caller with the import statement. The import statement takes        many different forms, shown below.

 ```
 import <module_name>
 ```
 ***dir() Function***

  The built-in function dir() returns a list of defined names in a namespace. Without arguments, it produces an alphabetically sorted list of names in the current local symbol table.

***Reloading a Module***

  For reasons of efficiency, a module is only loaded once per interpreter session. That is fine for function and class definitions, which typically make up the bulk of a module’s contents. But a module can contain executable statements as well, usually for initialization. Be aware that these statements will only be executed the first time a module is imported.
  ```
  >>> import mod
  a = [100, 200, 300]

  >>> import mod

  >>> import importlib
  >>> importlib.reload(mod)

  a = [100, 200, 300]
  ```
---
## pytest
---
 The pytest framework makes it easy to write small tests, yet scales to support complex functional testing for applications and libraries.

 ***the advantages of pytest***

  * Very easy to start with because of its simple and easy syntax.

  * Can run tests in parallel.

  * Can run a specific test or a subset of tests

  * Automatically detect tests

  * Skip tests

  * Open source

---
Done
---

[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)