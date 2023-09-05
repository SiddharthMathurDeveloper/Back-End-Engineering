# UML Diagram :
![Screenshot 2023-09-05 at 1 58 26 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/69b266ab-b33d-49d7-aa8b-0de4491cc52a)

# Description :
- The Simple Factory, also known as the Static Factory, is not considered one of the standard Gang of Four design patterns.
  
- In a Simple Factory, the client code requests an object from the factory by providing some information or a parameter, and the factory decides which concrete class to instantiate and return.


# Elements :

1. Product: This is the abstract or interface class that defines the common interface for all the objects that the factory can create. In the example I provided earlier, Animal is the product, and it has a method speak() that all concrete products must implement.

2. Concrete Products: These are the specific classes that implement the Product interface. In the example, Dog and Cat are concrete products. Each concrete product provides its own implementation of the speak() method.

3. Factory: The factory is responsible for creating instances of concrete products based on some input or condition. In the example, AnimalFactory is the factory class that creates Dog and Cat objects based on the provided animal_type.

4. Client: The client is the code that utilizes the factory to create objects. It does not need to know the details of how the objects are created; it simply calls the factory's creation method with appropriate parameters.










# Drawbacks and Issues of the Simple Factory Pattern

## Lack of Open-Closed Principle Compliance

The Open-Closed Principle states that classes should be open for extension but closed for modification. In the Simple Factory pattern, when you need to add a new type of product, you often have to modify the factory class, which violates this principle. This can lead to code changes in multiple places, increasing the risk of introducing bugs.

## Violation of Single Responsibility Principle

The Simple Factory typically places both the responsibility of creating objects and deciding which object to create in a single class. This violates the Single Responsibility Principle, which suggests that a class should have only one reason to change. As your factory grows to handle more product types, it can become less maintainable.

## Limited Extensibility

If you have many product types or need to introduce variations in object creation, the Simple Factory pattern can become unwieldy. You might end up with long if-else or switch statements in the factory, making the code hard to read and maintain.

## Tight Coupling

The client code often needs to know the specific types of products to request from the factory. This results in tight coupling between the client and the factory. Any change in product types or the factory itself may require changes throughout the codebase.

## Reduced Testability

Since the client code typically directly calls the factory's creation method, it can be challenging to unit test the client code in isolation. Mocking or substituting the factory can be difficult, especially if the factory is tightly integrated into the client code.

## Limited Flexibility

The Simple Factory pattern doesn't easily support complex object creation scenarios. If objects require complex initialization or need to be configured with dependencies, you may find it cumbersome to adapt the Simple Factory.

## Difficulty in Managing Dependencies

If your products have dependencies or require some form of dependency injection, the Simple Factory may not provide an elegant solution. Managing these dependencies within the factory can be problematic.

## Limited Error Handling

Error handling in the Simple Factory is often simplistic. If an invalid product type is requested, the factory typically raises an exception. More advanced error handling and recovery mechanisms may be needed in real-world applications.
