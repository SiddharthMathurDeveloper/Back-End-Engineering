# UML Diagram :
![Screenshot 2023-09-06 at 10 29 41 AM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/4653db59-5d69-4784-a891-4876eb342934)

# Definiation :
***Factory Method*** is a creational design pattern that defines an interface (or abstract class) for creating objects, but allows subclasses to alter the type of objects that will be created.
It provides an encapsulated way to delegate the responsibility of object instantiation to subclasses, promoting flexibility, and decoupling between the client code and the actual object creation.

The phrase "but allows subclasses to alter the type of objects that will be created" in the context of the Factory Method pattern means that this pattern provides a way for subclasses to decide which concrete class of objects to create without changing the overall structure of the code.

Here's a more detailed explanation:

In the Factory Method pattern, you have an abstract class or interface (often called the "Creator") that declares a factory method. This factory method is responsible for creating objects of a related type (usually implementing a common interface or inheriting from a common base class).

Concrete subclasses of the Creator class (often referred to as "Concrete Creators") implement this factory method. Each Concrete Creator can decide which specific class of objects to instantiate based on its own logic or requirements.

The client code interacts with the Creator through the factory method, requesting objects to be created. It does not need to know which specific class is being instantiated.

So, the "allows subclasses to alter the type of objects that will be created" means that different Concrete Creators can produce different types of objects, and you can easily introduce new Concrete Creators to extend the system with new object types without modifying existing code. This flexibility and extensibility are essential benefits of the Factory Method pattern.








# When to use :

# Pitfalls :

# Real World :
