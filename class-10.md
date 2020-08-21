Duckett JavaScript
Ch 10

# Error Handling & Debugging

## Order of Execution

**order of execution** - The order in which statements are processed. 

## Execution Contexts

There are 3 execution contexts

**Global Context** - code that is in the script but not in a function. There is only one global context in any page

**Function Context** - Code that is being run within a function. Each function has its own function context

**Eval Context** - text is executed in an internal function called ```eval()```

## Variable Scope

**Global Scope** - If a variable is declared outside a function, it can
be used anywhere because it has global scope. If you do not use the var keyword when creating a variable, it is placed in global scope.

**Function-Level Scope** - When a variable is declared within a function,
it can only be used within that function. This is because it has function-level scope.
 
 
## The Stack

* The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.

	1.  When a statement has to call some other code in order to do its job, the new task goes to the top of the pile of things to do
	
	1. Once the new task has been performed, the interpreter can go back to the task at hand
	
	1. Each time a new item is added to the stack, it creates a new execution context
	
	1. Variables defined in a function(or execution context) are only available in that function
	
	1. if a function gets called a second time, the variables can have different values
	

## Execution Context & Hoisting

2 phases of activity each time a script enters a new execution context

**Prepare** 

	The variables are determined and the value of the this word is determined
	
**Execute** 

	1. Assigns values to variables
   	2. References function and runs their code
	3. Execute statements
	
*The preparation phase is often described as taking all of the variables and functions and **hoisting** them to the top of the execution context.*

**variables object** - contains details of all the variables, functions and parameters for that execution context. 

In the interpreter, each execution context has its own variables object.
It holds the variables, functions, and parameters available within it.
	
Each execution context can also access its parent's variables object.

**lexical scope** - functions that are linked to the object they were defined within

for each *execution context*, the *scope* is the current execution context's variables object, plus the variables object for each parent execution context.	

Each time an outer function calls an inner function, the inner function can have a new variables object. But variables in the outer function remain the same.

There are 7 error objects:

They can be found on 460 and 461 of the javaScript book

```console.log``` shows code in the browser console and helps with finding errors.

A list of common errors is on page 485


https://deannaj401.github.io/reading-notes/


