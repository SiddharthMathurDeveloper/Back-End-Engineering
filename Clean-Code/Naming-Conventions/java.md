# Naming Conventions in Java

## 1. Package Names:
   - Package names should be in all lowercase letters.
   - Use a domain name you control in reverse order as the prefix to avoid naming conflicts.
   - Separate segments of the package name with dots.

   **Example:**
   ```java
   package com.example.projectname;
   ```



  ## 2. Class Names:
  - Class names should be in PascalCase (also known as UpperCamelCase), starting with a capital letter.
  - Use nouns or noun phrases that describe the class's purpose.

   **Example:**
   ```java
   public class EmployeeRecord {
    // Class implementation
  }
  ```



 ## 3. Interface Names:
 - Interface names should also be in PascalCase.
 - Use adjectives or adjective phrases that describe the interface's behavior.

 **Example:**
   ```java
   public interface Printable {
       void print();
   }
  ```



## 4. Method Names:
 - Method names should be in camelCase, starting with a lowercase letter.
 - Use verbs or verb phrases that describe the action the method performs.

 **Example:**
   ```java
   public void calculateTotalPrice() {
       // Method implementation
   }
  ```


## 5. Variable Names:
 - Variable names should be in camelCase.
 - Use meaningful and descriptive names to represent the data they store.

 **Example:**
   ```java
   int numberOfStudents = 25;
   String customerName = "John Doe";
  ```

## 6. Constant Names:
  - Constant (final) variable names should be in uppercase letters.
  - Separate words using underscores.
  - Use meaningful names that convey the purpose of the constant.

 **Example:**
   ```java
   public static final int MAX_RETRY_COUNT = 3;
   public static final String COMPANY_NAME = "ABC Corp";
  ```



## 7. Enum Types:
  - Enum types should be in PascalCase.
  - Use singular nouns or noun phrases that describe the enumeration.
  - Enum values should be in uppercase letters.
 **Example:**
   ```java
   public enum DayOfWeek {
       SUNDAY,
       MONDAY,
       // Other days of the week
   }
  ```

## 8. Boolean Variables and Methods:
 - Use prefixes like "is," "has," "can," or "should" for boolean variables and methods.


 **Example:**
   ```java
   boolean isAvailable = true;

   public boolean hasPermission() {
       // Method implementation
   }
  ```

## 9. Parameters and Arguments:
- Method parameters should be in camelCase, like regular variables.
- Be descriptive with parameter names, avoiding single-letter names when possible.


 **Example:**
   ```java
  public void printCustomerDetails(String firstName, String lastName) {
    // Method implementation
  }   
  ```


## 10. Getters and Setters:
 - For getter and setter methods, use the standard JavaBean naming conventions.
 - Getters start with "get" or "is" for boolean properties (e.g., isEnabled()).
 - Setters start with "set" (e.g., setName(String name)).


 **Example:**
   ```java
  public class Person {
    private String name;
    
      public String getName() {
          return name;
      }
    
      public void setName(String name) {
        this.name = name;
      }
  }
```



## 11. Exception Classes:
 - Exception classes should end with the word "Exception."
 - Avoid using "Error" at the end of custom exception class names, as it may be confused  
   with system-level errors.

 **Example:**
   ```java
   public class DataNotFoundException extends RuntimeException {
    // Exception implementation
  }
```


## 12. Lambda Expressions and Functional Interfaces:
 - For lambda expressions and functional interfaces, use descriptive names that convey the  
   purpose of the interface or functional method.

 **Example:**
   ```java
   // Functional interface with a single abstract method
@FunctionalInterface
public interface Calculator {
    int calculate(int a, int b);
}

// Usage of the functional interface with a lambda expression
Calculator addition = (a, b) -> a + b;
```



## 13. Collections and Iterables:
  - For collection and iterable variable names, use plural nouns to indicate that they represent multiple elements.

 **Example:**
   ```java
   List<String> names = new ArrayList<>();
  Set<Integer> uniqueNumbers = new HashSet<>();
  ```




## 14. Lambda Expressions and Functional Interfaces:
 - For lambda expressions and functional interfaces, use descriptive names that convey the  
   purpose of the interface or functional method.

 **Example:**
   ```java
   // Functional interface with a single abstract method
@FunctionalInterface
public interface Calculator {
    int calculate(int a, int b);
}

// Usage of the functional interface with a lambda expression
Calculator addition = (a, b) -> a + b;
```


## 15. Avoid Hungarian Notation:
 - Avoid using Hungarian notation, where variable names start with a prefix indicating their data type. This convention is considered outdated in modern Java.


 **Example:**
   ```java
   // Avoid Hungarian Notation
int iItemCount;
String strName;

// Preferred
int itemCount;
String name;
  ```


## 15. Avoid Underscores for Non-Constants:
 - For non-constant variables, avoid using underscores in their names.
 - Reserved for constant variables (e.g., MAX_RETRY_COUNT) as per convention.


 **Example:**
   ```java
   // Avoid
int total_items;

// Preferred
int totalItems;
  ```














