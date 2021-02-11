# QC
Quality Control Department
- 1on1 with Bach
- Groups of 3 with the trainers
  - 3-4 questions
  - they take notes about your and Bach's strengths and weaknesses.
- Expectations
   - Let Bach know when you have to miss class
   - Do your best
   - No plagerism
     - Do not reference past materials, make it all you
- How to do well...
   - ask questions
   - review "How to do well in QC."
   - practice, practice, practice
   - remember to be professional
   - **be kind and warm** *(note from you)*
# Git
A little more...
 - Work with branches
    - you can create and delete "branches"
    - each branch allows a space for you to put code that is part of the same project
    - you can also make any branch reflect into the 'main' branch
    - "commit" can be used as a "save point" for your work
    - git reset, resets to a previous time
    - commiting to git allows you a different and more manual option with more ability to change how you store data than your typical saving functions
    - look at git tutorials as branching and merging is very, very commmon and in good practice so look it up
    - naming convention for branches: "name-of-branch"
  
  # Java Operators
  Learn the UNLIMITED POWER of programming! Operate your primitives.
  - Arithmetic
  - Logical
  - Assignment
  - Relational (comparison)
  - Bitwise

## Arithmetic
MATH!

| Operator | Name      | Description             | Example |
| :------- | :-------- | :---------------------- | :------ |
| +        | ADD!      | ADD!                    | x + y   |
| -        | Subtract! | Minus!                  | x - y   |
| *        | Multiply! | You know how this works | x * y   |

## Logical (Spock)
Used to perform operations with booleans!

| Operator | Name        | Description                         | Example  |
| :------- | :---------- | :---------------------------------- | :------- |
| &&       | Logical AND | Returns true if the same            | x && y   |
| \|\|     | Logical OR  | returns true if ONE returns TREU    | x \|\| y |
| !        | Logical NOT | Returns false if the result is TRUE | !x       |
---
- Short-circuting operators
   - true ||... (always true, right side doesn't matter)
   - false &&... (always false, right side doesn't matter)
   - You can check for a short by setting up a short print boolean methods and run them through the operand
- Non short-circuting
   - using the single operands, however that would ask for more computing power. ex " & , \| "
  



## Assignment 
Used for assigning values... duh

| Operator | Example | Example   |
| :------- | :------ | :-------- |
| =        | x = 3   | x = 3     |
| +=       | x =+ 3  | x = x + 3 |
| -=       |
| *=       |
| /=       |
| %=       |

## Relational
Compare those suckers and get you a boolean return!

| Operator   | Name     | Example             |
| :--------- | :------- | :------------------ |
| ==         | Equal to | 2 == 2 returns true |
| !=         |
| >          |
| <          |
| >=         |
| <=         |
| instanceof |

## Bitwise
They exist. Look them up for extra credit!

| Operator | Example | Example |
| :------- | :------ | :------ |


## Statements v. Expressions
- Statement: int= x+y The whole assignment
- Expression: x+y the mathmatical section of a statement or the data before the function (anything that evaluates to a value)

# Java Control Flow
- Code within your methods are executed line by line from top to bottom on the order they appear. However, when it cpmes to programming, we often don't want things to execute in a straight line. **Control flow statements** allow us to break up the flow of execution by including decision making, looping, and branching abilities in order to enable oir program to conditionally execute blocks of code.

- Decision Making
   - if-then
   - if-then-else
   - switch
 - Looping
   - for loops
   - while loops
   - do-while loops
 - Branching
   - break
   - continue
   - return

## Decision-making Statements
- if-then
  - tells our program to execute a certain section od code only if the test evaluates to true
- if-then-else
  - gives our program a secondary path of execution if the test evaluates to false
- switch
   - simplifies the process of having multiple execution paths
   - works with *byte*, *short*, *char*, *int*, *enums*, *string*, and wrapper classes for Byte, Short, Character, Integer
   - There is the concept of "fall-through" with switch statements, where if we omit a break statement, you will execute subsequent cases
   - we can also have a default case which executes if no other cases are matched
  
#  If Statements
  - chaining if statements are done by using else if statements
  - nested if statements are allowed. Meaning you can place an entire if statement within another
## Switch
- creates a system of cases which will print if found true
- unlike if statements where the block ends when one thing if found true as switch statements will run all lines as long as they are found true
- break statements will help you control the fall through of switch statements enabling you to end it when you need to
## Loops
- for loops
- while loops
- do while loops

### For loops
 - allows for incremental expressions up to a designated point
 - example: if you run a machine to count up numbers to a specified limit then stop
 - "loops" processing until a point is reached and then is "broken"
 - any data declared within the loop stays in and cannot be used outside
    
  ```java
  for (<initialization>; <termination>; <increment/decrement>) {
      // code here
  }
  ```

- *initialization:* declares the data type for the statment
- *termination:* marks conditions that when met terminates the loop
- *increment/decrement:* defines how the data will adjust until termination

### While Loops
- creates a *while* condition where the loop will continue while the conditions are met
- if the condition is initially false it will never execute
  

  example:
```java
while (number > 0) {
    System.out.println("number: " + number);
    number--;
}
```
### Do While
- like a while loop but gaurantees at least one execution

## Branching Statements

### Break
- *break* is a way to break any loop at any moment. Using an if statement around a break will allow you to specify conditions for the break
- labeled and unlabeled *(see below)*

### Continue
- lets you continue the loop even when a false boolean is detected.
- can continue a number count after a condition aren't met
- labeled and unlabeled *(seebelow)*

### Labels (exampleLabel)
- this allows you transcend nested for loops.
- breakout of a loop with a nested loop on the inside by coupling with *break*
- continue from the top loop from a nested loop by coupling this with *continue*

### Return
- this is just a method return statement
- specifies the breaking boolean condition
- using return false will break and return false when the condition is met
- return true will break and return true when met

# Arrays
Sequential elements of the same type
- Arrays are fixed size objects
- ordered and indexed starting at 0
- size of array specified as int only
- can be multidemensional (arrays of arrays)
- length can be found by accessing the length field

## Declaring arrays
  ```java
  // declarations
  int myIntArray[];
  int[] myOtherIntArray; // more common

  // to instaniate
  myIntArray = new int[5];
  ```
  - to list the elements you can print it using the *toString* method. Otherwise you'll get some hashed memory code
  - if an array isn't set you'll get the defaults for each data type
    - 0 for int
    - 0.0 for doubles
    - false for boolean
    - null for objects in general
  - just listing the elements of the array can only work if you're both declaring and instatiating the array at the same time
  - 
example:
```java
char[] myCharArray = {'a','b','c'} //shorthand

char[] myCharArray;
myCharArray = {'a', 'b', 'c'} // will not work
```


## Multi-Dimensional Arrays
```java
int[][] the2DArray = new int {{1,2,3}, {4,5,6}, {7,8,9}};
System.out.println(the2DArray[2][0]);
```
This will print out 7 


# Things to look up:
1. Garbage collector
2. The Heap and The Stack
3. String Pool and memory allocation
4. Bitwise Operands
5. String buffer/builder?
6. for loops: continue operand
7. for loops: labels
8. enhanced for loops
9. difference between Java and C#
10. Var-Args
11. Enums
12. Constructors
