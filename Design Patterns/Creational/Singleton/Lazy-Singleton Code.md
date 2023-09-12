
## Question :
Implement a singleton pattern in Java for a class called Database. The Database class should have a private constructor and a public static method called getInstance(). The getInstance() method should return the singleton instance of the Database class.


## UML :



## Code :

### Client.java
```java
public class Client {
    public static void main(String[] args) {
        
        LazySingletonDatabase lazySingletonDatabase = LazySingletonDatabase.getInstance();

    }
}
```


### LazySingletonDatabase.java
```java
public class LazySingletonDatabase {
    private LazySingletonDatabase(){

    }

    private static class LazySingletonDatabaseHolder{
        static LazySingletonDatabase INSTANCE = new LazySingletonDatabase();
    }

    public static LazySingletonDatabase getInstance(){
        return  LazySingletonDatabaseHolder.INSTANCE;
    }


}
```
