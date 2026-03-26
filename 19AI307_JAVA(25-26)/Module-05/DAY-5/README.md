# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
You are asked to simulate a ticket booking system where multiple users (threads) try to book seats for an event. The system starts with a certain number of available seats. Each thread tries to book a given number of seats. You must ensure the booking is done safely using synchronization, preventing overbooking.

## AIM:
To simulate a ticket booking system using multithreading with synchronization to prevent overbooking.

## ALGORITHM :
1. Create a TicketCounter class with a synchronized method bookTicket().
2. Initialize total available seats in the counter.
3. Create a UserThread class where each thread requests seat booking.
4. In the synchronized method, check if enough seats are available; if yes, deduct seats and confirm booking.
5. If seats are insufficient, display a failure message.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```java
import java.util.*;

class TicketCounter {
    int availableSeats;

    TicketCounter(int seats) {
        availableSeats = seats;
    }

    synchronized void bookTicket(String name, int seats) {
        if (seats <= availableSeats) {
            availableSeats -= seats;
            System.out.println(name + " successfully booked " + seats + " seats. Remaining: " + availableSeats);
        } else {
            System.out.println(name + " failed to book " + seats + " seats. Only " + availableSeats + " available.");
        }
    }
}

class UserThread extends Thread {
    TicketCounter counter;
    String name;
    int seats;

    UserThread(TicketCounter counter, String name, int seats) {
        this.counter = counter;
        this.name = name;
        this.seats = seats;
    }

    public void run() {
        counter.bookTicket(name, seats);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int initialSeats = sc.nextInt();
        int users = sc.nextInt();

        TicketCounter counter = new TicketCounter(initialSeats);
        ArrayList<UserThread> list = new ArrayList<>();

        for (int i = 0; i < users; i++) {
            String name = sc.next();
            int seats = sc.nextInt();
            UserThread t = new UserThread(counter, name, seats);
            list.add(t);
            t.start();
        }

        for (UserThread t : list) {
            try {
                t.join();
            } catch (Exception e) {
            }
        }
    }
}
```






## OUTPUT:
<img width="1167" height="552" alt="image" src="https://github.com/user-attachments/assets/650ae384-174e-41c5-864f-5dfdb845551f" />



## RESULT:
The program safely handles multiple users booking tickets using synchronization, ensuring no overbooking occurs.
