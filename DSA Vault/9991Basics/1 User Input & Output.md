# 1 User Input & Output
Class:  [[Language Basics]]
Subject/Topic: #Language-Basics
Date: 2024-12-25
Link: [Basic Input and Output in Java - Tutorial](https://takeuforward.org/java/basic-input-and-output-in-java/)

Notes:

## Basic Input and Output in Java

Input and output operations enable Java programs to interact with users, making it possible to create user-friendly applications with **graphical interfaces** or **command-line interfaces**. Input allows programs to **obtain data** from various sources, such as **users**, **files**, or **external** **devices**. This data can be used for **processing**, **analysis**, or **storage**. Whereas, output enables programs to present results or information to users in a **readable and meaningful format**. This is essential for displaying **data**, **reports**, or **graphical visualizations.**

Java offers two input methods, **Scanner** and **BufferedReader**, to cater to diverse programming needs. Scanner **simplifies console input** for common use cases, providing easy-to-use methods for various data types. BufferedReader, on the other hand, offers greater control and efficiency, making it suitable for **complex input scenarios** and handling large volumes of data, such as reading from files or network streams. 

### **Including Libraries**

Java is a versatile language, that relies on libraries to access various functionalities. To perform tasks like input and output, we include specific libraries at the beginning of our code. One such essential library is **java.util**, which includes the **Scanner class**. The Scanner class is a workhorse for handling user input, allowing you to effortlessly read data from the keyboard or other sources.

### Using Scanner Class

#### Algorithm / Intuition

**The Generic Skeleton**

The generic skeleton of a Java program consists of two main components: **the import statements** and **the main method**. After importing the necessary libraries, you declare the main method using public static void main(String[] args) { /* Your code here */ }. This serves as the entry point for your program.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Your code here
    }
}
```

**Output with System.out.println**

To display output in Java, you'll commonly use the System.out.println method. There's no need to specify a namespace as in C++. For instance, System.out.println("Hey, Striver!"); will print "Hey, Striver!" to the console. You enclose the text you want to display within double quotation marks.

**Code:**

The **println** method automatically adds **a newline character** at the end of the printed text. So, each time you use **println**, the output will be on a new line.

**Code:**

As you can see, it will print "Hey, Striver!" to the console and then start a new line. The behavior of **println** is designed to make it convenient for **displaying text on separate lines in the console**.

### **Taking User Input Using Scanner**

One of the fundamental aspects of programming is **taking input from the user.** In Java, this is achieved with the help of the **Scanner class,** which allows you to receive input from the user via the terminal or console.

**Code:**

When you run this Java program and enter a value (e.g., 10) in the terminal, the **Scanner** **class** captures that value, stores it in the variable x, and then displays it using System.out.println. Here's how it works:

1. The program waits for user input.
2. You enter a value (e.g., 10) and press Enter.
3. cin reads the entered value and stores it in the variable x.
4. cout then displays the value of x.

To accept multiple inputs in Java, we can use the **nextInt()** method of the Scanner class for each variable we want to receive input for. Let's demonstrate this by taking two variables, x and y, as input and displaying their values:

**Code:**

When you run this Java program and enter two values (e.g., 10 and 20) in the terminal, the Scanner class captures both values, stores them in the variables x and y, and then displays their values using System.out.println.

You might be wondering about the meaning of "int x" and "int y." We will dive into the topic of data types in Java in the next topic. Stay tuned!

### **Note:**

To use commonly used utility classes in Java, you can import the java.util package.

**import java.util.*;** imports all classes and interfaces from the java.util package. 

You can then use classes from the **java.util** package, such as **Scanner**, **ArrayList**, **HashMap**, and others, as needed in your Java program. Importing only the classes you use can help keep your code more **efficient** and **maintainable**, as you won't have unnecessary overhead from importing unused libraries.

However, it's essential to be aware of **potential compatibility issues** and consider the **impact on compile time**, especially in large Java projects. When you import a broad range of classes or packages, it can lead to longer compilation times and potential conflicts if different classes have the same name in different packages. Therefore, in Java, it's best practice to import only the specific classes or packages you need for your program.

Using Buffered Reader

Algorithm / Intuition

BufferedReader is more efficient when dealing with **large volumes of input data**, such as reading from files or network streams. It reads input as a **stream of characters** and can be particularly useful for handling text-based data where you need to **parse lines or process data incrementally**. BufferedReader also provides greater control over the input process, allowing you to handle exceptions and errors more gracefully. It's commonly used in scenarios where **input performance and robust error handling are crucial.**

### **Creating a BufferedReader Object**

To use **BufferedReader**, first, we create an object of the InputStreamReader class. This object specifies where the input originates from.

InputStreamReader is = new InputStreamReader(System.in);

Here **InputStreamReader** **object** ‘is’ designates input from the keyboard. System.in represents the **standard** **input**, which is usually your keyboard. But it could be something else, like a file or network stream, depending on what you point it to.

### **Initializing BufferedReader**

Now, create a **BufferedReader** **object** and pass the **InputStreamReader** **object** into it. This BufferedReader will be responsible for reading and processing the input.

InputStreamReader is = new InputStreamReader(System.in);
BufferedReader bf = new BufferedReader(in);

Here, the **InputStreamReader** class is used to convert the **raw byte-based input** stream (System.in) into a **character-based input stream**. This is necessary to read text input conveniently.

Now, the **BufferedReader** is used to **buffer the input stream**, making it more efficient to read lines of text. It provides methods like **readLine()** to read complete lines of text, which is very useful for user input.

### **Reading Numerical Input**

To read numerical input from the user, we use the **readLine()** method. However, this method **returns a string**, so you'll need to convert it to an integer using **Integer.parseInt()**.

**Code:**

![](https://static.takeuforward.org/wp/uploads/2023/10/java-bufferedreader-1024x847.png)

This flowchart illustrates the process of **taking user input** and **converting it to an integer**. It begins with the creation of an **InputStreamReader** object to read input from the standard input, followed by the creation of a **BufferedReader** object for efficient input handling. The flow then proceeds to read a line of input using the **readLine()** method of the BufferedReader. After obtaining the input as a string, the flowchart shows the crucial step of using **Integer.parseInt()** to convert the string into an integer. This flowchart provides a clear visual representation of a common input-handling scenario in Java.



