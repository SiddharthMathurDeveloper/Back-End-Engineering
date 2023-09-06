# UML Class Diagrams
- Link [https://www.youtube.com/watch?v=j84w5VM9GT8&t=0s]
- Link [https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-class-diagram-tutorial/]
- Link [http://www.cs.utsa.edu/~cs3443/uml/uml.html]






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



## Interface & Abstract

![Screenshot 2023-09-03 at 10 50 53 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/0bf003ee-f708-4c2a-8151-9a8b68dfe052)

- For Abstract Class replace Interface word with that word Abstract





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
   


## Multiplicity :
- Multiplicity is used to indicate the number of instances of one class that can be associated with the instances of another class in an association relationship. It defines the cardinality of the relationship between classes.

- Multiplicity is typically represented using numbers, asterisks (*), or intervals. Here are some common multiplicity notations:

### Exact Cardinality: You can represent the exact number of instances using integers. For example:

1: Indicates that there is exactly one instance associated.
0..1: Indicates that there can be zero or one instance associated.
2: Indicates that there are exactly two instances associated.
Asterisk (*) for Zero or More: An asterisk (*) is used to indicate zero or more instances. For example:

### *: Indicates that there can be zero or more instances associated.
Range or Interval: You can specify a range or interval using two integers separated by two dots (..). For example:

### 1..3: Indicates that there can be between 1 and 3 instances associated.
Unspecified or Unlimited: Sometimes, you might see an infinity symbol (∞) or the keyword "unlimited" used to represent an unspecified or unlimited number of instances. For example:

### 0..* or 0..∞: Indicates zero or more instances.
1..* or 1..∞: Indicates one or more instances.
Here's an example of how multiplicity can be represented in a UML class diagram:

  ### Example :  
   ![Screenshot 2023-09-02 at 6 46 03 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/256d579c-8d9d-4289-809d-34e702e15718)


![Screenshot 2023-09-02 at 6 46 22 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/f7822662-e248-44be-a9b6-83d0f69c4f09)



## has - a
- Class A `has -a` instance of Class B , think of either `aggregation` or `composition`

### Aggregation :

x![Screenshot 2023-09-02 at 6 59 50 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/0029e8ac-2fcf-4574-9aa6-7cf3b8e9a94b)
<br/>

- In this B `can` exist Without A
- Eg. Person has a House , Even if Person Object is destoryed House Object will still remain


### Composition (Part of) :
![Screenshot 2023-09-02 at 6 59 57 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/a0f15dba-25e4-40ed-9466-0d5e9da8a896)
<br/>
- Also can be called Part of A [in this case]
- In this B `can not` exist Without A
  
  ![Screenshot 2023-09-02 at 7 06 38 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/4ac012ff-0e29-4540-a490-bb4e72cacfbf)
<br/>
- Eg . Eye can't exist without Body as Eye is part of body , When body object is create then Eye is created when Body
  object is destoryed then Eye object is destoryed.


***They sometimes can be subjective (depends on what you are designing)***

```txt
If you see a class can belong to multiple classes then you understand that it can't be a
composition it will aggregation relationship only
eg -> Person and House , you can think a Person has a House should be composition , But if you thin that house instance will there in 3-4 instances of Person [like sister, brother, Mother..etc] so that House will be in instances of different people, not a composition ,

So If a instance is in mutliple object then not composition , but Aggregation
```




## Inheritance (is-a) :
![Screenshot 2023-09-02 at 7 22 22 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/b46b3cbe-458f-4e6f-af38-7c453738a4f4)
<br/>

## Interface
![Screenshot 2023-09-02 at 7 26 11 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/fc178bc0-54e5-4cab-83db-f57fc1f1e62e)
<br/>
- Just make Dotted Line instead of Solid Line

- Two ways to delcare in class Box

- Delcare in `ITALIC` , or
- <<ClassName>> this way inside <<>>









## Uses
![Screenshot 2023-09-02 at 6 52 26 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/81d9377d-0193-4daa-93b2-1e553e7e798a)

- Used in high level Design not adding to much detail , just telling the upper thing

### Bi-Direction 
```
    Uses
A--------------B
```

### Uni-Direction
```
      Uses
A -------------> B
```

## Role

    
  

  















