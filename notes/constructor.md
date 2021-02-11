# Java: Condtructors
When we use the `new` keyword to create an object, the JVM invokes a special class member called a **constructor**. A constructer declares how an object is to be instantiated and initialized from the class blue print.
- Condtructors are declared like methods, but methods signature does not contain a return type
- Constructors always have the same name as the class it id defined in

just like methods we can overload constructors with varying number of parameters / types

## Associated Keywords
 - `this` keyword
    - can be used for constructor chaining when invoked as a methed (eg. this(..parameters))
    - to refer to the object itself
       - This is usually done to avoid "variable shadowing" problems
 - `super` keyword
   - references the parent classs
   - when invoked similarly to a method (es. super(..parameters)), the parent class constructor is called
   - could also be used to refer to instance variables defined in  the parent class
 - "The Default 'no-args' constructor"
   - If we don't define the constuctor, the default constructor is provided automatically by the compiler
   - this is known as the default no-arguments constructor
   - NOTE: If we define any constructor in our class, this will NOT be provided

## Types of Constructors
1. Default constructor (no-args) No return type
2. User defined no-args constructor
   - If we define any other constructors, the default will not be provided
   - So if we still want to have no-args constructor, we need to provide our own
3. Parameterized constructor
    - These are constructors that we define with parameters
    - Often ised to set properties at the time  of instantiation
4. Copy Constructor
    - used to take another object and clone its properties into this current object being instantiated

