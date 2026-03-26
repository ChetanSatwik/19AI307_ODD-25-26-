# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

## AIM:
To simulate a Radar Control Tower system using the Singleton pattern ensuring only one instance handles all flight communications.

## ALGORITHM :
1. Create a class RadarControlTower with a private static instance variable.
2. Make the constructor private to prevent multiple object creation.
3. Provide a public static method getInstance() to return the single instance.
4. Create a method to handle flight communication (e.g., requestLanding).
5. In the main method, multiple flights access the same instance and communicate with the tower.




## PROGRAM:
 ```java
/*
Program to implement a SOLID Principles in Java Program
Developed by: N V Chetan Satwik
RegisterNumber:  212224240100
*/
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private int flightCount = 0;

    private RadarControlTower() {}

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();  
        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```

## SOURCE CODE:







## OUTPUT:
<img width="1246" height="279" alt="image" src="https://github.com/user-attachments/assets/57b37306-e866-432a-bf82-79d74fc3df1f" />



## RESULT:
All flights successfully communicate with a single shared Radar Control Tower instance, ensuring consistency and safety.
