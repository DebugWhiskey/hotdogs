# Notes: Feb 11th 2021
Yeah NOTES!
# Encapsulation
1. Containing related state and behavior together inside a class
    - Can help us adhere to SRP (Single Responsibility Principle)
2. Hiding and preventing change to an object's data members
    - Prevents arbitrary external changes that could cayse an object ro be in an invalid/inconsistent state
      - e.g. imagine we have a Person class, and some code arbirtarily changes a Person object's age to a negative value

Encapsulation introduces the idea of **getter** and **setter** methods. Getter methods are used to access private members from the outside, while setter methods would allow us to modify. Access to the getter and setter methods themselves are also controlles by access modifiers. Usually these getters and setters might be `public`.

# String API
Strings in JAVA are not primitives unlike some other programming languages. They are **immutable** objects that are instantiates from the `String` class.

Immutable: cannot be altered once created.
- Accomplished using
  - private and final fields
  - not implementing "setter" methods
- Implications of immutability for Strings: all methods in the String call that return a String return a brand **new String** every time.
  - We cannot change a String object's actual value, so a new string must be generated with the desired modifications

## String API methods
- `concat(String str)`: concatenate strings together
  - returns a completely new string
  - some string + another string
- `startsWith`
  - `startsWith(String prefix)`
  - `startsWith(String prefix, int offset)`
- `endsWith(String suffix)`
- `contains(CharSequence s)`: returns true if a string contains that particular sequence of characters
- `charAt(int index)`: return a char at a given position of the string
- `matches(String regex)`: returns true if the string matches a given **regular expression**
- `substring(int beginIndex)`: returns a portion of the string as another string starting at some index
- `substring(int beginIndex, int endIndex)`: returns a portion of the string starting a given index to the last index (NOT INCLUDING the end index)

# String Builder - Buffer
*stared at line 8

Since we are not doing multi-threading, we can simpply use StringBuilder instead, because it is faster.

 | Class         | Immutable? | Safe? | Speed       |
 | :------------ | :---: | :---: | :---------- |
 | String        | Y          | Y     | **Slowest** |
 | StringBuilder | N          | N     | **Fastest** |

# Generics
Added in Java 5 to provide compile time checking and also helps remove rthe risk of ClassCastException. This allows us to acheive type-safety, especially when using `Java Collections`.

Java allows us to define classes with generic types, which are classses or interfaces that are parameterixed. We can use angle brackets to specify parameter type.

# Collections Frameworks
The Collections framework is a set of classes **and** interfaces in Java that implement commonly used data structures. Below is a diagram showing the collection hierarchy. The most important interfaces are the followin:
- `iterable`: guarantees that the collection can be interated over
- - `collection`: the parent interface of all the collection, EXCEPT Map/ Map is seoerate from this hierarchy
- `list`: is an interface that extends the collectrion interface. It represents data structures that are ordered, similar to an Array. Lists can append to with more elements, and do not have fixed size.
- `set`: a collection that does not contain dup;icate elements. If you try to add an element that already exixts in the Set, it will simply not add it. The elements are not necessarily ordered, except in the case of TreeSet.
- `Queue`: a collection that operates on a first-in-firts-out (FIFO) basis, just like people waiting in a line.
- `map`: contains key/value pairs and **is a separate from the collection hierarchy**. However it does belong to the collections framework


![Collections Framework](https://javaconceptoftheday.com/wp-content/uploads/2014/11/CollectionHierarchy.png?x70034)

## Collection v. Collections
- Collection: the interface that all of the collections except for map inherit from
- Collections: a utility 

 
---
---
# Questions / Things to look up:
  1. String Builder - Buffer
  2. toString()
  3. class v. interface
  4. 


## Practice:
1. 
