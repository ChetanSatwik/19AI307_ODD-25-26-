# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely finds an ancient vault secured by binary locks. Each lock responds to bitwise operations to determine whether it opens or stays shut.

To unlock the vault, she is given two integers that represent key codes in binary. The vault uses the following bitwise operations to test them:

Lock Test                           Operator
Bitwise AND                            &
Bitwise OR                             |
Bitwise XOR                            ^
Left Shift first key by 1              <<
Right Shift second key by 1            >>

She needs to apply these operations and report the results.

Input Format:
First line: First key (integer)

Second line: Second key (integer)

Output Format:
Bitwise AND: <result>
Bitwise OR: <result>
Bitwise XOR: <result>
First Key << 1: <result>
Second Key >> 1: <result>

## AIM:
To write a Python program to perform bitwise operations (AND, OR, XOR, left shift, and right shift) on two given integers.

## ALGORITHM :
1. Start the program.

2. Read two integers a and b from the user.

3. Compute a & b, a | b, and a ^ b for bitwise AND, OR, and XOR.

4. Compute a << 1 (left shift of first key) and b >> 1 (right shift of second key).

5. Display all the results and stop the program.



## PROGRAM:
 ```java
import java.util.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        System.out.printf("Bitwise AND: %d\n",a&b);
        System.out.printf("Bitwise OR: %d\n",a|b);
        System.out.printf("Bitwise XOR: %d\n",a^b);
        System.out.printf("First Key << 1: %d\n",a<<1);
        System.out.printf("Second Key >> 1: %d",b>>1);
    }
}
```

## Sourcecode.java:







## OUTPUT:
![alt text](image.png)

## RESULT:
The program successfully performs bitwise operations (AND, OR, XOR, left shift, and right shift) on two given integers and displays the results.

