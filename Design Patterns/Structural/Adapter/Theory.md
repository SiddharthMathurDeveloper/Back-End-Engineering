
***Two Way to implement Class Adapter Way or Object Adapter Way**

# UML Diagram :
![Screenshot 2023-09-20 at 10 59 55 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/e65ebe9d-e45b-4b3c-8279-7aa6c97e79a5)

<br/>

![Screenshot 2023-09-20 at 11 00 15 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/349875d2-c523-48d6-85a7-ffed7753485e)

# Definiation :
The Adapter Design Pattern is a structural design pattern in software engineering. It is used to enable the interaction between two incompatible interfaces or classes by providing a wrapper (the "adapter") that acts as an intermediary between them. The primary goal of the Adapter Pattern is to make two existing interfaces work together without modifying their source code.








# When to use :

### Multiple Related Product Families:
When your application needs to create families of related or interdependent objects, and you want to ensure that the products within each family are compatible with each other.

Key components of the Adapter Pattern include:

Target Interface: This is the interface that the client code expects to interact with. It defines the methods or operations that the client code calls.

Adaptee: The Adaptee is the class or interface that needs to be adapted to work with the client code. It's the existing class that is incompatible with the client's requirements.

Adapter: The Adapter is a class that implements the Target Interface and encapsulates an instance of the Adaptee. It translates the calls made by the client code to the appropriate methods of the Adaptee.

There are two common approaches to implementing the Adapter Pattern:

Class Adapter: In this approach, the Adapter is implemented as a subclass of both the Target Interface and the Adaptee. It inherits from the Adaptee and provides an implementation of the Target Interface.

Object Adapter: In this approach, the Adapter contains an instance of the Adaptee and delegates the calls from the Target Interface methods to the corresponding methods of the Adaptee.

The Adapter Pattern is useful in scenarios where you have existing classes or components with different interfaces that need to work together. It allows you to achieve compatibility and reuse existing code without making substantial changes to it. This pattern is commonly used when integrating third-party libraries, legacy code, or when you want to create a more flexible and maintainable system by decoupling client code from specific implementations.



# Pitfalls :


### Performance Overhead: 


# Real World :

### GUI Frameworks
In a graphical user interface (GUI) framework like Java Swing, you can find abstract factories for creating UI components such as buttons, text fields, and windows. Different look-and-feel themes provide concrete implementations of these factories.






