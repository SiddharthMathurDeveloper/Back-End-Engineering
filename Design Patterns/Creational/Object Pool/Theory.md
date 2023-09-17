# UML Diagram :

![Screenshot 2023-09-07 at 6 14 45 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/7a9ddc6f-2929-4f42-94a3-c5c82279a77c)

# Definiation :
***Prototype Method*** The Prototype pattern is a creational design pattern that deals with creating new objects by copying an existing object, known as a prototype. 
Instead of using constructors or factory methods to create new objects, the Prototype pattern allows you to create new objects by copying an existing object, known as a prototype.





# When to use :
### Object Initialization Overhead: 
When creating objects from scratch is expensive in terms of time or resources, and you want a more efficient way to create new objects that share common properties with existing objects.





***Remember that the Prototype pattern allows you to create new objects by copying existing ones, saving time and resources. However, it's important to ensure that the prototype object is in a consistent and valid state before cloning it. Additionally, not all objects are suitable for cloning, especially if they have complex internal dependencies or external resources that cannot be easily duplicated.***



# Pitfalls :
## Shallow vs. Deep Cloning

Depending on your requirements, you may need to implement either shallow cloning (copying references to internal objects) or deep cloning (recursively copying all internal objects). Choosing the wrong approach can lead to unexpected behavior.





# Real World :

1. **Operating System Processes:** In modern operating systems, processes are often created by cloning an existing process (the parent process) to save time and resources.





