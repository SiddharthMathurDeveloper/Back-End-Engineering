

# UML Diagram :
![Screenshot 2023-09-12 at 6 32 29 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/4e9f528b-66f6-472e-8335-2f6de70255bd)



# Definiation :
***Early or Eager Instantiation:*** In this type of singleton, the instance is created at load time. This is the simplest way to implement a singleton, but it can have performance implications, as the instance is created even if it is not immediately needed.

***Lazy Instantiation:*** In this type of singleton, the instance is created only when it is required. This is more efficient than early instantiation, but it can be more complex to implement.









# When to use :

### Multiple Related Product Families:
When your application needs to create families of related or interdependent objects, and you want to ensure that the products within each family are compatible with each other.





# Pitfalls :


### Performance Overhead: 
Depending on the language and implementation, there can be a slight performance overhead associated with using abstract factories, as they involve additional method calls and object instantiation.



# Real World :

### GUI Frameworks




