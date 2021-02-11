## Wk. 1 Monday Java Notes 2.8.21
- Always recompile when making changes

## Git Repository
How to set your repository.
- Create and open bash in folder
- *git init* into bash to create .git file
- Create repository on GitHub.com
- 

# Spring Tool Suite 4
Using the IDE
- Setup
  - Make sure to not only select your appropriate JRE, but also the corralating Compiler.
  - You can select the specific JRE by using the *Configure JREs...* link in the JRE window and then browsing to your chosen JRE.
  - Then when the warning comes up at the bottom use it's provided link to change to the correct Compiler.
- The Main Method
  - Everything runs through the Main Method
  - When programming any methods written need to get passed back into main() to run. It's the code's way of telling the computer to "run this, this way!"
  - The Main Method is only required in ONE class, but make sure it's in the class that acts as the "gateway" for the application.
  - When running methods through the main you only need to name the method in the main().
  -To run or *"invoke"* a method from another class you have to declare the class first followed by "." then the method name.
  - *"Class"* + *"."* + *"methodName()"*
  - Class.methodName();

- Methods and Classes
  - Classes are like the blue prints that can be used to instantiate objects into a method.
  - Methods are used inside the classes to define the parameters and behavior for each "Blueprint."

  # Java Data Types
  At a high level, there are two main groups of data types. These are the following:
   - Primitive data types
   - Reference data types

   Primitice data types are fundamental data types in Java that make up the building blocks for other types. Think back to the idea of classes, which at as blueprints--

   Think of chemistry, for example. In our various mixtures we can have amix of compounds, molecules, atoms, etc., but ultimately at some point, everything reduces down to atoms. Atoms are analogous to the idea of primitives.

   ## Primitives
   - Built into the language
   - Foundation of all other types
   - Four categories of primitives: 
     - Integer types (integral types)
     - Floating point types (decimal numbers)
     - Character type
     - Boolean type
  - Stored by value

Passed by values and stored by value is important to understand for primitives, because not all languages treat primitive data types this way


---

**Integer Types**

| Type | Bits | Min Value | Max Value | Literal Form | 
| :--- | :--- | :--- |:--- | :--- |
| byte | 8 bits | -128 | 127 | 0 |
| short | 16 bits | -32768 | 32767 | 0 |
| int | 32 bits | -2,147,483,648 | 2,147,483,647 | 0 |
| long | 64 bits | -9,223, 371,036,854,775,808 | 9,223, 371,036,854,775,808 | 0L |

---
**Floating Point Types ?**

---

# Java: Classes v. Objects
- Java has the constructs of clsses and objects built into the language.
  - Objects: represented--

## Strings
- Strings are not primitives in Java
- Strings are actually objects
   - There is a String class built into Java that serves as a blueprint for all String objects

- Therefore, when we have a variable of a String type. it is actually a reference type variable. --

#Casting
In Java, at high level, we have two forms of casting:
- Explicit casting
- Implicit casting

Casting can be performed  on both primitivevs and reference data types. Although primitive convcersion and reference variable casting look similar, they are actually very different conceptually.

In both cases, we "turn" one type into another, but primitive variables actually contain a value, which results in actual changes to its value.

## Primitive Variable Casting
Primitve casting is also known as type conversion. This allows us to change the value from one data type to another. Impilicit casting occurs if we go from primitive data type that is "smaller" in range to one that is "larger" in range. In more technical terms , implicit casting occurs when the casting is "safe", while explicit casting is necessary if it is "unsafe".

- Widening conversion
  - Occurs implicitly
  - byte -> short -> char -> int -> long -> float -> double
  - Note how long fits inside float, despite long being 64bits, while float is only 32
- Narrowing Conversion
   - Occurs Explicitly
   - Care should be taken when converting from a wider primitive to a narrower primitive
   - double -> float -> long -> int -> char -> short -> byte

## Reference Variable Casting
This is where we convert from one reference type to another. in the case of reference variable casting, implicit casting occurs if we go from a child class up to a paren tclass, which is  "safe". Explicit is from parent to child which is "unsafe"/

NOTE: This will make more sense as you learn

- Unlike primitive casting, reference casting doesn't modify or touch the object itself, only the variable that is pointing to the object.
   - Reference casting simply labels the object in a different way
   - It either expands or narrows the methods/properties--


