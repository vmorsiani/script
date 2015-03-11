# Searle Script
basic scripting language designed for ChatBots

to Run
```
mvn exec:java
```
example apps are in
```
src/main/resources/
```

##Language Syntax

**Note:** the language ignores white space

###Operators (In order of Precedence)
* (*expression*) - evaluate *expression* first, changes order of operations
* ->  - get element from a JSON Map - can also be on the left side of an assign to modify the JSON map
* [*expression*] - get index from JSON array specified by *expression* - can also be on the left side of an assign to modify the JSON array
* function *param* - all functions take one parameter, if *param* is an expression it should be surrounded by ()
* ++ - Post Increment
* -- - Post Decrement
* * - Multiply
* / - Divide
* % - Modulo
* + - Add
* - - Subtract
* . - String Concatenation
* > - Greater Than
* < - Less Than
* == - Equals
* != - Not Equals
* = - Assign
 
###Data Types
All variables are stored as strings, and parsed as integers or JSON as required by operators.  Conditional operators consider "0" or "" to be false and everything else to be true

* "quoted string" - a string, can have \t\n\" as escape characters
* rand - returns a random positive integer
* *variable* - if declared with var, evaluates to it's curent value


###Commands

commands should be terminated by ;


* var *token* [ = *expr*] - declares *token* as a variable, can also include an assignment
* {command;*} - command block, allows for several commands to be treated as one command
* if (*expression*) command [ else command ]  - executes command if *expression* is true, can have optional else block
* while (*expression*) command - executes command while *expression* is true
* get *url* - returns the body of the HTTP response of *url* as a string
* *expression* - expressions such as i++;

