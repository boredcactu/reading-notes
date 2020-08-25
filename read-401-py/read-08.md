# Game of Greed 3

## List Comprehensions in Python

List comprehensions provide a concise way to create lists.

It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

The result will be a new list resulting from evaluating the expression in the context of the for and if clauses which follow it.

The list comprehension always returns a result list.

If you used to do it like this:
```
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))

```
You can obtain the same thing using list comprehension. Notice the append method has vanished!
```
new_list = [expression(i) for i in old_list if filter(i)]

```
### Syntax

The list comprehension starts with a ‘[‘ and ‘]’, square brackets, to help you remember that the
result is going to be a list.

The basic syntax uses square brackets.


```
[ expression for item in list if conditional ]
```

This is equivalent to:


```
for item in list:
    if conditional:
        expression
```

>let us explore what is happen with this shortcut code:

```
new_list = [expression(i) for i in old_list if filter(i)]

```

1. ***new_list***
The new list (result).

1. ***expression(i)***
Expression is based on the variable used for each element in the old list.

1. ***for i in old_list***
The word for followed by the variable name to use, followed by the word in the
old list.

1. ***if filter(i)***
Apply a filter with an If-statement.

This [blog](http://blog.cdleary.com/2010/04/learning-python-by-example-list-comprehensions/) shows an example of how to visually break down the list comprehension:

list comprehensions, how you can use it:

- Create a list using loops and list comprehension
- Multiplying parts of a list
- Show the first letter of each word
- Lower/Upper case converter
- Print numbers only from a given string
- Parsing a file using list comprehension
- Using list comprehension in functions




## ***references:***
1. [List Comprehensions](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)


Done
---
 
[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)