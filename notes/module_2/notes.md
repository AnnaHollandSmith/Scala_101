# Module 2: Basic Object Oriented Programming

**2.1:**
```
Objectives:

● Create and instantiate classes in Scala
● Describe how arguments are passed to Scala class instances
● Outline the lifespan of class parameters in a Scala class instance
```
**What is a Class?**
- A class is a description of a Type
 - Embodies state in an instance of a class
 - Represents behaviour for how that state can be transformed
 - It is not concrete until it has been 'instantiated' via a call to its constructer via the 'new' keyword
 Multiple instances of a class can exist


 _Eg. A customer: Inside of a customer you might have states such as their name or their address or their phone number. Classes represent behaviour for how that state can be transformed. For example, how you might change someone's address or their name. Classes are not concrete unless they have been instantiated by a call to their constructor with the 'new' keyword. The class merely describes how you would want to represent concepts such as a customer and then to have an instance of a customer that represents a specific person you have to instantiate the Customer class with the new keyword_

**The Primary Constructor:**

 - Each class gets a primary constructor automatically
  - Defines the 'signature' of how to create an instance
  - The body of the class is the implementation of the constructor (within the curly braces)

**Class Parameters:**

- You can pass values into an instance of a class using one or more parameters to the constructor
 - You must specify the type of the parameter
 - The values are internally visible for the life of the class instance
 - They cannot be accessed from outside of the class instance

**2.2:**
```
Objectives:

● Describe the difference between mutable and immutable fields
● Create fields in Scala classes
● Describe the difference between class parameters and fields
● Outline how to promote class parameters to fields
```
**What is a field?**

- A value encapsulated within an instance of a class
 - Represents the state of an instance, and therefore an application at a given time
 - Is accessible to the outside world, unless specified otherwise

 **Field versus Parameters**

 - Parameters are passed to a class and are only visible within a class
 - Fields exist within the body of a class, and are accessible to outsiders

 _Mutable fields:_ can be set within the body using **var**<br>
 _Immutable fields:_ can be set using **val**

**Immutable or Mutable?**

- Immutable fields cannot be changed and are therefore "threadsafe" in a multithreaded environment, such as the JVM
- Mutable fields can be useful, but require diligence to ensure that multiple threads cannot update the field at the same time

**Specify Types**

- Scala has 'type inference' but it is best not to rely on this
- It is a good habit to be specific about types anyway

**Promoting Class Parameters:**

- If you want to make a parameter passed to a class constructor into a publicly visible field, add the val word in front of it
- The Scala compiler will generate an accessor method for you, and other class instances can now ask for the current state of the promoted field

[Scala Docs on Mutable and Immutable Collections](http://docs.scala-lang.org/overviews/collections/overview.html)

**2.3:**
```
Objectives:

● Implement methods in Scala
● Describe evaluation order of methods versus fields in Scala
● Outline how infix notation works in Scala
```

**What is a method?**

A method describes behaviour within a class :
  - Are something that can be called to do work
  - Where transformations to internal state can take place
  - May take parameters as inputs, and may return a single values
  - Should specify the return type
   - More correctness
   - Faster compilation


**Why Methods Instead of Fields?**

- Methods can look like Fields
- Methods are evaluated at the time they are called
- Methods are re-evaluated every time they are called
- Fields are only evaluated at the time the class is constructed, and if immutable, only one time

**2.4:**
```
Objectives:

● Utilize default argument values in Scala class constructors and methods
● Leverage named arguments to only pass certain values
```

**2.5:**
```
Objectives:

● Create Singleton objects in Scala
● Describe the difference between a class and an object in Scala
● Outline usages for objects in Scala applications
● Start a Scala application
```
