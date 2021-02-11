# The Tree Pillars of OOP: Inheritance
The process by which classes; can **inherit** the behavior of other classes. **base/parent/super** class and **child/sub**

## Terminology
- Base/Parent/Super: The class others inherit from
- Sub/Child: A class tht inherits
- IS-A relationship: (A dog **is an** Animal)

All **NON-private** fields and methods are inherited from a parent class.

Can 

The main benefit: reusability of code.

Helps us **`D.R.Y.`** (Don't Repeat Yourself)

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



# Encapsulation
1. Containing related state and behavior together inside a class
    - Can help us adhere to SRP (Single Responsibility Principle)
2. Hiding and preventing change to an object's data members
    - Prevents arbitrary external changes that could cayse an object ro be in an invalid/inconsistent state
      - e.g. imagine we have a Person class, and some code arbirtarily changes a Person object's age to a negative value

Encapsulation introduces the idea of **getter** and **setter** methods. Getter methods are used to access private members from the outside, while setter methods would allow us to modify. Access to the getter and setter methods themselves are also controlles by access modifiers. Usually these getters and setters might be `public`.
# Abstraction
A principle in which we centralize common characteristics and generalize behavior into conceptual modules. By utilizing abstraction, we hide underlying implementation.
When we drive a car we don't need to know how it runs, the car abstracts awau the internal details of timing, engine cycles, cooling, combustion, etc.

## Abstract Classes (pickup from here)