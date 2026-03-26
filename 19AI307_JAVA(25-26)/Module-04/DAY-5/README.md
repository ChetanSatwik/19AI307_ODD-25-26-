# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento design pattern in Java to save and restore the state of an article.

## ALGORITHM :
1. Create a ArticleMemento class to store the state of the article.
2. Create an Article class (Originator) to set, save, and restore content.
3. Create a Caretaker class to maintain a list of saved states.
4. Read multiple article contents from the user and store each version as a memento.
5. Retrieve a specific version and restore the article or display an error if invalid.




## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: N V Chetan Satwik
RegisterNumber: 212224240100
*/
```

## SOURCE CODE:
```java
import java.util.*;

class ArticleMemento {
    private String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        content = memento.getContent();
    }

    public String getContent() {
        return content;
    }
}

class Caretaker {
    private List<ArticleMemento> history = new ArrayList<>();

    public void addMemento(ArticleMemento m) {
        history.add(m);
    }

    public ArticleMemento getMemento(int index) {
        if (index < 0 || index >= history.size()) {
            return null;
        }
        return history.get(index);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Article article = new Article();
        Caretaker caretaker = new Caretaker();

        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            article.setContent(sc.nextLine());
            caretaker.addMemento(article.save());
        }

        int version = Integer.parseInt(sc.nextLine());

        ArticleMemento m = caretaker.getMemento(version);

        if (m == null) {
            System.out.println("Invalid version");
        } else {
            article.restore(m);
            System.out.println(article.getContent());
        }

        sc.close();
    }
}
```






## OUTPUT:
<img width="1096" height="552" alt="image" src="https://github.com/user-attachments/assets/f6e78415-e0fe-4ba2-92f3-06dd24d3a0e1" />



## RESULT:
The program successfully saves multiple versions of an article and restores a selected version using the Memento behavioral design pattern.
