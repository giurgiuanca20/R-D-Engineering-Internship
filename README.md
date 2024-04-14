# R-D-Engineering-Internship

1. **Explain the difference between a stack and a queue. Provide real life examples of real-life scenarios where each of them are used appropriately.** <br>
A *stack* is a linear data structure that follows the Last-In-First-Out (LIFO) principle. It's like a stack of papers, you have to take the first, then the second paper, etc. You can't take the last one without taking them all first. <br>
A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle. It's like a line(queue) at the store, first come, first served. <br>

2. **What is the difference between an array and a linked list? Provide advantages and disadvantages of each data structure.** <br>
An *array* is a static data structure, meaning the size is fixed at the time of creation. It allows fast access to elements but inserting and deleting elements can be slow as elements need to be shifted. <br>
A *linked list* is a dynamic data structure, meaning the size can change during the execution of the program. It allows fast insertion and deletion of elements but accessing elements can be slower compared to arrays. <br>


3. **What is HTTP? How is it different from HTTPS?** <br>
*HTTP* stands for Hypertext Transfer Protocol. It’s a protocol used for transmitting hypermedia documents on the internet. However, it is not secure. <br>
*HTTPS* stands for Hypertext Transfer Protocol Secure. It’s the same as HTTP but provides a layer of security using SSL/TLS protocols. <br>

   
4. **Can you give some examples of common HTTP response codes?** <br>
*200 OK:* The request has succeeded. <br>
*404 Not Found:* The server can not find the requested resource. <br>
*500 Internal Server Error:* The server encountered an unexpected condition. <br>

5. **What is the difference between authorization and authentication?** <br>
*Authentication* is the process of verifying the identity of a user. <br>
*Authorization* is the process of verifying what a user has access to. <br>

6. **How would you explain to a 5-year-old how the WWW works?** <br>
I would say that it is like a genie that can show or teach you almost anything, you tell it what you want and it shows you. <br>


7. <br>
public class Main {
    public static void printStaircase(int n) {
        for (int i = 1; i <= n; i++) {
            for (int j = 0; j < n - i; j++) {
                System.out.print(" ");
            }
            for (int k = 0; k < i; k++) {
                System.out.print("#");
 //                   System.out.print(" ");   //for appearance
            }
            System.out.println();

        }
    }
    public static void main(String[] args) {
        printStaircase(5);
    }
}

8. <br>
```java
import java.lang.Math;

public class Main {
    public static void encrypt(String text) {
        text = text.replaceAll("\\s", "");

        int L = text.length();

        int row = (int) Math.floor(Math.sqrt(L));
        int column = (int) Math.ceil(Math.sqrt(L));

        if (row * column < L) {
            row += 1;
        }

        for (int i = 0; i < row; i++) {
            for (int j = 0; j < column && i * column + j < L; j++) {
                System.out.print(text.charAt(i * column + j));
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        String text = "if man was meant to stay on the ground god would have given us roots";
        encrypt(text);
    }
}
