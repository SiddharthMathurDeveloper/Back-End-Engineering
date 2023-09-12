

## Question :
Implement a singleton pattern in Java for a class called Database. The Database class should have a private constructor and a public static method called getInstance(). The getInstance() method should return the singleton instance of the Database class.



## UML :



## Code :

### Client.java
```java
public class Client {
    public static void main(String[] args) {
        EagerSingletonDatabase eagerSingletonDatabase = EagerSingletonDatabase.getInstance();
        EagerSingletonDatabase eagerSingletonDatabase2 = EagerSingletonDatabase.getInstance();

        System.out.println(eagerSingletonDatabase2==eagerSingletonDatabase);

    }
}
```


### EagerSingletonDatabase
```java
public class EagerSingletonDatabase {

    private EagerSingletonDatabase(){}

    private static final EagerSingletonDatabase INSTANCE = new EagerSingletonDatabase();
    public static EagerSingletonDatabase getInstance(){
        return INSTANCE;
    }
}
```













