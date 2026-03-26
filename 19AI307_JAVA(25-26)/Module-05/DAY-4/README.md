# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

## AIM:
To create two threads, set their names based on user input, and assign priorities (4 for t1 and 2 for t2).

## ALGORITHM :
1.	Create a class that extends Thread.
2.	Read thread names for t1 and t2 from the user.
3.	Create two thread objects and assign the user-given names.
4.	Set priority 4 for t1 and priority 2 for t2.
5.	Start both threads and display their name and priority.




## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class MyThread extends Thread {
    MyThread(String name) {
        super(name);
    }
    public void run() {
        System.out.println(Thread.currentThread());
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        MyThread t1 = new MyThread(name1);
        MyThread t2 = new MyThread(name2);

        t1.setPriority(4);
        t2.setPriority(2);

        t1.start();
        try {
            t1.join();
        } catch (Exception e) {}

        t2.start();
    }
}
```






## OUTPUT:

<img width="820" height="263" alt="image" src="https://github.com/user-attachments/assets/109f2ece-559e-429f-99dc-6fd69cc79535" />


## RESULT:
Two threads are created with user-defined names, and their priorities are set to 4 and 2 respectively and displayed successfully.
