# Ex.No:3(C) ABSTRACTION

## QUESTION:
In a secret facility, you are designing intelligent agents that can explore grid-based mazes. Each agent sees the maze differently and interprets it using their unique instinct.

You are to build a system using abstraction where a base class MazeAgent declares an abstract method:

abstract String generateNavigationCode(String[] maze);
Two agents – ScoutAgent and HunterAgent – extend this class, but behave very differently.

Agent Behaviors
ScoutAgent
This agent is highly sensitive to special signals placed in the maze. Every time it senses the signal (@), it records where (which corridor row) the signal was found.
The final navigation code is the sequence of all those rows where it felt the signal — encoded as numbers.

HunterAgent
This agent is on the lookout for how trapped it might be. It keeps a strict count of all obstructions it sees in the maze walls.
If the number of such obstructions is equal or more than 10, it believes it's been trapped. Otherwise, it considers itself safe to escape.

🛠️ Your Task:
Implement the abstract class and its derived classes.

Accept maze rows as input.

Create the agent based on input.

Print the navigation code they generate.

Input Format:
n
maze_row_1
maze_row_2
...
maze_row_n
type
n = number of rows in the maze

Each maze_row_i = a string containing symbols (like #, ., @)

type = 1 for ScoutAgent, 2 for HunterAgent

Output Format:
A string representing the navigation code as computed by the selected agent. -

For HunterAgent - "TRAPPED"/ "ESCAPE"

## AIM:
To design a Java program using abstraction where different maze agents (ScoutAgent and HunterAgent) analyze a maze and generate a navigation code based on their specific behaviors.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an abstract class MazeAgent with the abstract method generateNavigationCode(String[] maze).
4.	Create two subclasses ScoutAgent and HunterAgent that implement the method with their specific behaviors.
5.	In ScoutAgent, scan each row of the maze and append the row number whenever the symbol @ is found.
6.	In HunterAgent, count the number of # symbols in the maze and return "TRAPPED" if the count is ≥ 10, otherwise return "ESCAPE".
7.	In the main method, read the maze rows and agent type, create the appropriate agent object, call the method, and print the navigation code.





## PROGRAM:
 ```java
/*
Program to implement a Abstraction using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
import java.util.*;

abstract class MazeAgent {
    abstract String generateNavigationCode(String[] maze);
}

class ScoutAgent extends MazeAgent {
    public String generateNavigationCode(String[] maze) {
        StringBuilder code = new StringBuilder();
        for (int i = 0; i < maze.length; i++) {
            if (maze[i].contains("@")) {
                for (char ch : maze[i].toCharArray()) {
                    if (ch == '@') {
                        code.append(i + 1); 
                    }
                }
            }
        }
        return code.toString();
    }
}

class HunterAgent extends MazeAgent {
    public String generateNavigationCode(String[] maze) {
        int wallCount = 0;
        for (String row : maze) {
            for (char ch : row.toCharArray()) {
                if (ch == '#') wallCount++;
            }
        }
        return wallCount >= 10 ? "TRAPPED" : "ESCAPE";
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); sc.nextLine(); 
        String[] maze = new String[n];
        for (int i = 0; i < n; i++) {
            maze[i] = sc.nextLine();
        }
        int type = sc.nextInt(); 

        MazeAgent agent = (type == 1) ? new ScoutAgent() : new HunterAgent();
        System.out.println(agent.generateNavigationCode(maze));
    }
}
*/
```

## SOURCE CODE:







## OUTPUT:
![alt text](image.png)


## RESULT:
The program analyzes the maze using the selected agent (ScoutAgent or HunterAgent) and outputs the corresponding navigation code or escape status.
