# Notes: Feb. 10th 2021
Thoughts and follow along. Hopefully I'll get all I need.

# Debug
Learn to debug by isolating code and stepping through the code to find what's wrong.
 - Set **breakpoints** then start **debug** and when it stops begin to check through the paused code by **stepping**.
 - Using controls in the IDE you can run through your program (application) step by step.
 - This allows you to run through the code as it runs step by step, line by line.
 - Breakpoints:
   - Setting a breakpoint allows you to pause the execution of the code at a specific line helping you to more accurately debug.
 - Compilation errors: Bad syntax
 - **Exceptions**: Occur at runtime, is a problem with the variables or code setup. Ex. trying to divide by zero.
# Wrapper Classes
Allow us to  represent primitives as objects. Important for learning data structures in the **Java Collection API**, *which can only store objects and not primitives*.
- Wrapper classes are part of the java.lang pckg
- Conversion between a wrapper object and a primitive occurs automatically
  - **autoboxing**: primitive to object
  - **unboxing**: object to primitive

## Wrapper *utility methods/fields
    *Utility methods are static methods/classes used only for static utility. Such as math methods and classes. Not meant to be instantiated.
## Fields
- MAX_VALUE: constant holding the max values that the particular wrapper/primitive object can have.
- MIN_VALUE: Take a guess...
- SIZE: number of bits
- TYPE: *Class* instance representing primitive type

## Methods (static)
- valueOf(..): parses some argument into a wrapper object
- parseInt(..), parseDouble(..), ... : parse some argument into a primitive of that type
- intValue, doubleValue, longValue, etc.: returns value of wrapper object as a primitive

## Collections
## Array Lists
- Only stores objects (wrap any primitives to add to the list)


# Packages and Imports
Packages are used to group related classes. Packages are like folders. They group similar code as well to prevent naming conflicts in order to promote maintainability.
- Built in packages  from the JRE
- User-defined packages

Imports allow us to use clsses from other packages. The `import` keyword tells the JVM what class to use from where. We also have `import static` which allows us to import static methods or static variables to use directly without needing to refer to them by `Classname.<whatever>`.

# Access Modifiers
Help to restrict accessibility of a class, constructor, field, or method. Four access modifiers exist.
1. public
   - Allows for access anywhere 
2. protected
   - Access within same package and subclasses outside that package
3. default
   - Access mod when we don't give one.
   - Access from any class in the same package
   - The `default` keyword is different from the default access mod
4. private
   - Allows access **only** within the same class


    **Tip:** Go from least restrictive to most to help understand them better: Public > Protected > Default > Private

# Variable Scopes
    Essentially 4 different types of scope to be aware of. Here they are from least specific to most.
 1. Static Scope
   - Refers to a variable that belongs to the class itself
   - Any other scope below static can access variables in the statis scope
2. Instance Scope
   - Variables that belong to a particular instance/object
   - Can access static variables as well as instance variables
   - can also invoke static methods from within instance methods
3. Method Scope
   - Variables declared within a method
   - Whenever a method is done executing, the variable is no longer in scope and is basically gone
4. Block Scope
   - Variables defines within a block of code
     - if statements
     - for loops
     - while loops
     - etc.

# Polymorphism
"Taking on many forms" In programming this describes how objects can behave differently in different contexts.
- Method Overloading (compile-time polymorphism)
- Method Overriding (run-time polymorphism)
  
## Method Overloading
Where two or methods in the same class with the same method name, but different method signatures in the for parameters.
(Not really polymorphism as the only simliarity is the name in which you call it by which isn't seen by the compiler and so are technically different methods entirely.)


## Method Overriding
The case in which the child class has the same method signature as a method in the parent class. However this method in the child class can have a different implementation. Child classes can change the default behaviour, which makes class hierarchies and inheretance more flexible and dynamic.

    Very powerful practice for creating applications.

When overriding a parent method in a child class, the method must:
- Have a covariant return type
  - the return type must be the same or subclass of the return type in the parent method
- The same method name
- The same method parameters
- The same access modifier or more access


## Covariant Return types
When we override a method, we can actually change its return type, as long as the return type is a **subclass** of the original return.

# Annotations
Special (optional) constructs that are seen in Java. Use th `@` symbol followed by annotation name. They are used to provide metadata about source code to the compiler and/or JVM. They can be placed on classes, methods, fields, and other constructs depending on how these annotations were defined.

One of the primary purposes of annotations is to enforce rules in the code or to abstract away some functionality provided by a framework (for example, Spring framework). Annotations are often processed using Java's built-in `Reflection API` to dynamically provide functionality for developers.

A few annotations:
- `@Override`: declares that a method must override an inherited method.
- `@Deprecated`: marks a method as obsolete
- `@SupressWarnings`: instructs compiler to suppress compilation warnings
- `@FunctionalInterface`: designates an interface to be a functional intereface

# Reading from the console w/ Scanner
Scanner is a class found in the java.util package that is used to read input data from different sources. (eg. console input, files, etc.)

Scanner takes an InputStream object in its constructor, so when we are instantiating this object, we will pss in a special InputStream corresponding to our console.

## Methods
- nextLine(): returns a string containing the text entered on the line of input
- next(): read the next token/word in the input
- Primitive reads:
  - nextByte()
  - nextShort()
  - nextLong()
  - nextInt()
  - nextDouble()
  - nextFloat()
  - nextLine()
- nextLine() is part of everyother next*Primitive*() function. So whenever scanner reads one of the other types it'll automatically enter a nextLine() to enter a new line. This means however that everytime you use a nextLine() after another one it'll skip the nextLine() and count it.
  - To circumvent this you can either wrap the variable and use only nextLine().
  - OR you can simply put an extra nextLine() after any other next*Primitive*() you place.

# Object Class
Specific class that is the root class of all other classes. Other classes either **directly or indirectly** inherit from this `object` class.

## Methods
The Object class has some important methods.
- `toString()`: auto-called when we print a reference variable. If this method is not overridden (polymorphism), it will print the output as `<fully qualified class name>@hasedMemoreyAddress`
- `equals(Object o)`: compares two objects. It .equals(Object o) is not being
- `hashcode()` returns hash code, a number that is used for putting objects into finite numbers of categories. Hashcodes are used in HashMaps, HashSets, and other data structures.

Some rules for hashcode():
- **If we override equals(), hashCode(), should also be overridden to the same properties.**
- hashCode() should also have a predictable result.

1. If two objects are equal to .equals(), they MUST have the same hashcode value.
2. If two object are not equal, they do not necessarily have to have different hashcode values.

The Object class also has a `finalize()` method that is called by the garbage collector. We *would* override to perform cleanup, but don't need to.

# Final Keyword
 The `final` keyword is a type of **non-access** mod that can be used when declaring an entity. It means that the value connot be modifier after. Final can be used on variables, parameters, methods, and classes

 ## Final varirables
 When declared with the final keyword it cannot be reassigned once initialized.
 - Does not need to be initialized at the same time as declaration.
 - Once assigned it cannot be reassigned
 - Reference variables go unchanged, but the object it's referring to can be.

## Final Parameters
Same deal, once used and initialized in a method it cannot be changed.

## Final Methods
- Cannot be overridden (instance method)
- Cannot be blehgk
---
---
# Questions / Things to look up:
  1. Debugging
   2. Java class naming conventions
   3. java.lang package
   4. final non-access modifier
   5. Wrapping autoboxing and unboxing
   6. *"Source not found" - **Answer:** attach the src.zip file from the jdk folder.* 
   7. Generic Types
   8. instance method vs normal **ANSWER:**  **Instance Methods** belong to objects as **Static Methods** belong to the class. `'Instance method are methods which require an object of its class to be created before it can be called. To invoke a instance method, we have to create an Object of the class in within which it defined.'` *-geeksforgeeks.org* // **Instance Methods** belong to objects as **Static Methods** belong to the class.


## Practice:
1. Overriding / Inheritance