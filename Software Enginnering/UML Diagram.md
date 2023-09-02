# UML Class Diagrams






# Class :
![Screenshot 2023-09-02 at 2 03 36 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/66967a4d-475c-4c6d-af4a-d487ab393472)

<br/>

- A box divided into 3 parts
1. First Section (Class Name)
2. Second Section (Properties / attributes)
3. Third Section (Functions / Methods)
 
    




## Access Modifiers :

- Plus (+) means `Public`
 ``` java
+ publicMethod()
+ publicAttribute
 ```

- Minus (-) means `Private`
 ```java
- privateMethod()
- privateAttribute
 ```
- Hashtag (#) means `Protected`
 ```java
# protectedMethod()
# protectedAttribute
```

- Tilde (~) means `Default`
```java
~ packagePrivateMethod()
~ packagePrivateAttribute
```

## Functions / Methods:

 
### Without Args :
```
Operation():Return Type 
```
- Function Name with bracket Because it is function [Operation()]
- SemiColon to seperate the Name and Type [:]
- Then the Return Type of function [Return Type]
  Example
   ```txt
   // Checking if engine is on or off
   EngineStatus(): Boolean 
   ```
   
### With Args :
```
Operation(args):Return Type :
```
- Function Name with bracket Because it is function [Operation()]
- Args with the brackets [args]
- SemiColon to seperate the Name and Type [:]
- Then the Return Type of function [Return Type]
  Example
   ```txt
   // Checking if engine is on or off
   EngineStatus(int value): Boolean 
   ```

## Static 
- use an underline (e.g., _staticMethod(), _staticAttribute) or a
- specific stereotype like <<static>> above the member name to indicate that it's static.





# Relationship :


## Association :

![Screenshot 2023-09-02 at 6 34 49 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/71545106-694f-4f35-9396-d7903e3c0e0c)

### Bi-Direction 
![Screenshot 2023-09-02 at 6 34 21 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/d561d263-b1a8-4a8e-b467-e813c633babf)

 - A ------------ B this is how association is presented.
 - Meaning that both the classes can call each other , A can call B or B can call A.

### Uni-Direction 
![Screenshot 2023-09-02 at 6 34 02 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/f77bf26a-2643-4e4b-a010-f3ac0f0c54a1)

 -  A ------------> B , Where A can access B but B can't access A ,
 -  A <------------ B , Where B can access A but A can't access B,

   ***Where arrow which points tell that this can that class on start end can class Class on end , not vice-versa.
    A ------------> B Start = A , End = B (A can B , but B can't A).***
   


   





  
    
  

  















