# Java : Methods and Parameters
Methods are blocks of code that only run when they are called. The `public static void main(String[] args)` method, however, is a special method that is called directly by the JVM when we run our application. The purpose of utilizing methods, is to reuse code by defining it only once then reusing it. 
- Methods must be declared wthin a class in Java
- Methods are defined with an access modifier, followed by any non-access modifiers, the return type, and then the name of the method and the parethesis can define the various parameters a method may accept.
- `<access modifier> <non-access modifier> <return type> <method name> (<parameters...>) { // code here}`

## Method Overloading 
Methods with duplicater names. Allows for same functionality with different parameters.
- have different parameter types

**AND/OR**

- have a different number of parameters

by following the above guidelines there is not ambiguity.

## Var-Args
Stands for variable-arguements, which allows for us to set an indefinite amount of variables.
- ...nums
