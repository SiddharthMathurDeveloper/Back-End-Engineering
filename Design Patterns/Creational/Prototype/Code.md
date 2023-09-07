
## Question
You are designing a role-playing game (RPG) where players can customize their characters with various attributes, appearances, and equipment. To optimize character creation and improve gameplay, implement the Prototype design pattern to create a CharacterPrototype system. Explain how this pattern allows players to efficiently create and customize new characters while reducing object creation overhead. Provide a class diagram and describe the key classes and their responsibilities in your design.

In your response, discuss how the Prototype pattern enables players to clone existing character templates and modify them to suit their preferences, showcasing how it enhances gameplay and reduces resource consumption. Also, consider any potential use cases where the Prototype pattern might be extended or combined with other design patterns to further improve the gaming experience.

## UML :




## Code :

### Client.java
```java
public class Client {
    public static void main(String[] args) throws CloneNotSupportedException {
        Soldier soldier1 = new Soldier(10,"Sword",70);
        soldier1.setAbility("Shield move");
        System.out.println(soldier1);


        Soldier soldier2 = (Soldier) soldier1.clone();
        System.out.println("Cloned Sword Men");
        System.out.println(soldier2);


        King king = new King(10,"Hammer AXe",70);
        System.out.println(king);



        King king2 = (King) king.clone();;
        System.out.println(king2);

    }
}
```


### CharacterPrototype.java
```java
public abstract class CharacterPrototype implements Cloneable {

    private int height;
    private String weapon;

    private int health;

    public CharacterPrototype(){
        this.health=0;
        this.weapon="Knife";
        this.health=20;
    }

    public CharacterPrototype (int height, String weapon, int health) {
        this.height = height;
        this.weapon = weapon;
        this.health = health;
    }

    public int getHeight() {
        return height;
    }

    public void setHeight(int height) {
        this.height = height;
    }

    public String getWeapon() {
        return weapon;
    }

    public void setWeapon(String weapon) {
        this.weapon = weapon;
    }

    public int getHealth() {
        return health;
    }

    public void setHealth(int health) {
        this.health = health;
    }


    @Override
    public CharacterPrototype clone() throws CloneNotSupportedException {
        try {
            CharacterPrototype characterPrototype = (CharacterPrototype) super.clone();
            characterPrototype.initialize();
            return characterPrototype;
        } catch (CloneNotSupportedException e) {
            throw new AssertionError(e);
        }
    }


    // reset the state
    protected void initialize(){
        this.health=0;
        this.weapon="Knife";
        this.health=20;
        reset();
    }

    protected abstract  void reset();
}
```


### Soldier.java
```java
public class Soldier extends CharacterPrototype {


    private String ability = "Stand";



    public Soldier(int height, String weapon, int health) {
        super(height, weapon, health);
    }

    @Override
    protected void reset() {
        ability = "stand";
    }

    @Override
    public String toString() {
        return "Soldier height is " + getHeight() +  " is health " +  getHealth() + " and Weapon                                               is " + getWeapon() + " Ability is " + getAbility();
    }

    public String getAbility() {
        return ability;
    }

    public void setAbility(String ability) {
        this.ability = ability;
    }
}
```


### King.java
```java
public class King extends CharacterPrototype {


    private String ability = "King Last Stand";


    public King(int height, String weapon, int health) {
        super(height, weapon, health);
    }

    public String getAbility() {
        return ability;
    }

    public void setAbility() {
        this.ability = ability;
    }

    @Override
    protected void reset() {
        throw new UnsupportedOperationException("Should not be called");
    }


    @Override
    public String toString() {
        return "King height is " + getHeight() +  " this " +  getHealth() + " and Weapon is " + getWeapon() +" ability is " + getAbility();
    }


    @Override
    public CharacterPrototype clone() throws CloneNotSupportedException {
      throw  new CloneNotSupportedException("Cloning not support");
    }

}
```






