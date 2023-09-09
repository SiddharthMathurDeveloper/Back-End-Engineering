
## Question :
You are working on the development of a World War II-themed strategy game in the style of Hearts of Iron (HOI). The game involves multiple factions, each with distinct units, technologies, and strategies. Implement the Abstract Factory design pattern to create a FactionFactory system that allows for the creation of faction-specific units, technologies, and strategies. Provide a class diagram and describe how the Abstract Factory pattern enhances modularity and facilitates the addition of new factions to the game.

In your response, explain how the Abstract Factory pattern ensures that faction-specific content, such as units and technologies, can be created seamlessly while maintaining a high level of cohesion and minimizing code duplication. Discuss how this design pattern can simplify the addition of new factions to the game and how it promotes a clean and organized codebase for managing diverse gameplay elements in a World War II context within the HOI game.


## UML :



## Code :




### Client.java
```java
package Creational.AbstractFactory;

public class Client {

    public static void main(String[] args) {
        Factory factory = new Factory(new SovietUnitFactory());

        GameUnitFactory gameUnitFactory = factory.getGameUnitFactory();

        Infantry infantry = gameUnitFactory.createInfantryUnit();
        infantry.weapon();


    }
}
```


### Factory.java
```java
public class Factory {

    private GameUnitAbstractFactory gameUnitAbstractFactory;

    public Factory(GameUnitAbstractFactory gameUnitAbstractFactory){
        this.gameUnitAbstractFactory = gameUnitAbstractFactory;
    }

    public GameUnitAbstractFactory getGameUnitFactory(){
        return gameUnitAbstractFactory;
    }

}
```


### GameUnitAbstractFactory.java
```java
public interface GameUnitAbstractFactory {
    Infantry createInfantryUnit();
    Tank  createTankUnit();
}
```

### GermanUnitFactory.java
```java
public class GermanUnitFactory implements GameUnitAbstractFactory {


    @Override
    public Infantry createInfantryUnit() {
        return new GermanInfantry();
    }

    @Override
    public Tank createTankUnit() {
        return new GermanTank();
    }
}
```


### SovietUnitFactory.java
```
public class SovietUnitFactory implements GameUnitAbstractFactory {

    @Override
    public Infantry createInfantryUnit() {
        return new SovietInfantry();
    }

    @Override
    public Tank createTankUnit() {
        return new SovietTank();
    }
}
```

### Infantry.java
```java
public interface Infantry {

    enum UnitType{light , medium , heavy}
    void uniform();
    void weapon();
    void specialAbility();

}
```


### GermanInfantry.java
```java
public class GermanInfantry implements Infantry {

    @Override
    public void uniform() {
        System.out.println("Wearing gray-green wool field uniform");
    }

    @Override
    public void weapon() {
        System.out.println("Having a kar98k rifle");
    }

    @Override
    public void specialAbility() {
        System.out.println("blitzkrieg");
    }
}

```



### SovietInfantry;
```java
public class SovietInfantry implements Infantry {
    @Override
    public void uniform() {
        System.out.println("Wearing uniform M43");
    }

    @Override
    public void weapon() {
        System.out.println("Having a ppsh-41 rifle");
    }

    @Override
    public void specialAbility() {
        System.out.println("Mass Charge");
    }
}
```


### Tank.java
```java
Public interface Tank {

    enum TankType {light,medium,heavy};

    void name();

    void cannon();

    void armor();
}

```


### SovietTank.java
```java
public class SovietTank implements Tank {
    @Override
    public void name() {
        System.out.println("Soviet IS-2");
    }

    @Override
    public void cannon() {
        System.out.println("Soviet 122mm");
    }

    @Override
    public void armor() {
        System.out.println("Soviet Armor");
    }
}
```

### GermanTank.java
```java
public class GermanTank implements  Tank {
    @Override
    public void name() {
        System.out.println("German King Tiger");
    }

    @Override
    public void cannon() {
        System.out.println("German 88 Kwk");
    }

    @Override
    public void armor() {
        System.out.println("German Armor");
    }
}
```














