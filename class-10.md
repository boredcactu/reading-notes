# JS Debugging

## Error Handling 
*JavaScript can be hard to learn and everyone makes mistakes when writing it. This chapter will help you learn how to find the errors in your code. It will also teach you how to write scripts that deal with potential errors gracefully*

## order of execution :

To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex

## Execution Context :

The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope. 

## The Stack :

the javaspript interpreter processes one line of code at time 
When a statement needs data from another function;
it stacks the new function on top of the current task

## Understanding Scope :
In the interpreter, each execution context has its own va ri ables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's v a ri ables object. 

## Understanding Errors :
If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code


---

[home](/README.md) | [About me](/about-me.md) | [contact me](/contact-me.md)