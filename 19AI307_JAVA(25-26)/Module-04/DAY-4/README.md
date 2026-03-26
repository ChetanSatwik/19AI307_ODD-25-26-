# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a system that builds Car and Bike objects for two companies: "Honda" and "Yamaha". Use Abstract Factory Pattern to choose the brand and output the type and brand for each vehicle.

## AIM:


## ALGORITHM :
1. Create interfaces Car and Bike with a method getDetails().
2. Implement concrete classes like HondaCar, HondaBike, YamahaCar, and YamahaBike.
3. Create an abstract factory interface VehicleFactory with methods createCar() and createBike().
4. Implement factory classes HondaFactory and YamahaFactory to produce respective vehicles.
5. In the main method, select the factory based on brand and display vehicle details.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

interface Car {
    void assemble();
}
interface Bike {
    void assemble();
}

class HondaCar implements Car {
    public void assemble() { System.out.println("Honda Car created"); }
}
class YamahaCar implements Car {
    public void assemble() { System.out.println("Yamaha Car created"); }
}
class HondaBike implements Bike {
    public void assemble() { System.out.println("Honda Bike created"); }
}
class YamahaBike implements Bike {
    public void assemble() { System.out.println("Yamaha Bike created"); }
}

interface VehicleFactory {
    Car createCar();
    Bike createBike();
}

class HondaFactory implements VehicleFactory {
    public Car createCar() { return new HondaCar(); }
    public Bike createBike() { return new HondaBike(); }
}

class YamahaFactory implements VehicleFactory {
    public Car createCar() { return new YamahaCar(); }
    public Bike createBike() { return new YamahaBike(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String brand = scanner.nextLine().toLowerCase();

        VehicleFactory factory;
        if (brand.equals("honda")) factory = new HondaFactory();
        else if (brand.equals("yamaha")) factory = new YamahaFactory();
        else {
            System.out.println("Invalid company");
            return;
        }

        factory.createCar().assemble();
        factory.createBike().assemble();
    }
}
```






## OUTPUT:
<img width="617" height="338" alt="image" src="https://github.com/user-attachments/assets/412828ae-1317-4278-9a53-d4e884776ede" />



## RESULT:
Car and Bike objects are successfully created for Honda and Yamaha using the Abstract Factory Pattern, displaying their type and brand.
