## Practical No.1
#### Aim: - Demonstrate a default, overloaded and copy constructor.
###### A)Write a program to create a class and implement a default overloaded and copy constructor in Java

```
class Practical1
{
int num1 , num2 , result;
String UserName;
int UserAge;
String UserAdd;
Practical1() //Default contructor
{
num1 = 10;
num2 = 5;
result = num1+num2;
System.out.println("Inside Defualt Constructor");
System.out.println(result);
}
Practical1(int a , int b)
{
num1 = a;
num2 = b;
result = num1 + num2;
System.out.println("2para Constructor");
System.out.println(result);
}
Practical1(String name, int age, String address)
{
UserName = name;
UserAge = age;
UserAdd = address;
System.out.println("3para Constructor");
System.out.println("Welcome "+UserName+ ". Your Age is " + UserAge+ ". You
live in " + UserAdd);
}
public static void main(String[]args)
{
Practical1 obj1 = new Practical1(); // Calling Defualt Constructor
Practical1 obj2 = new Practical1(15,10); // Calling 2 parameterised Constructor
Practical1 obj3 = new Practical1("Asjad",21,"Mumbra"); // Calling 3 parameterised Constructor
}
}

```


## Practical No.1
###### B) write a program to create a class and implement the concept of method overloading


```
class Practical1_B
{ int num1 , num2 , result;
String UserName;
int UserAge;
String UserAdd;
void Data() //No parameterised Method
{
num1 = 10;
num2 = 5;
result = num1+num2;
System.out.println("Inside Defualt Constructor");
System.out.println(result);
}
void Data(int a , int b) // 2 parameterised Method
{
num1 = a;
num2 = b;
result = num1 + num2;
System.out.println("2para Constructor");
System.out.println(result);
}
void Data(String name, int age, String address) // 3 parameterised Method
{
UserName = name;
UserAge = age;
UserAdd = address;
System.out.println("3para Constructor");
System.out.println("Welcome "+UserName+ ". Your Age is " + UserAge+ ". You
live in " + UserAdd);
}
public static void main(String[]args)
{
Practical1_B obj = new Practical1_B();
obj.Data();
obj.Data(7,3);
obj.Data("Asjad",21, "Thane");
}
}


```

## Practical No. 2
#### Aim: - Demonstrate the concept of static methods
###### A) Write a program to create a class and implement the concept of static methods


```
class GFG {
static int a = 40; // static variable
int b = 50; // instance variable
void simpleDisplay()
{
System.out.println(a);
System.out.println(b);
}
static void staticDisplay() // Declaration of a static method.
{
System.out.println(a);
}
public static void main(String[] args) // main method
{
GFG obj = new GFG();
obj.simpleDisplay();
 staticDisplay(); // Calling static method.
} } 

```
## Practical No. 2
###### B) write a program to implement the concept of inheritance and method overriding.

```
class Grandpa {
void show()
{
System.out.println( "Inside show() method of Grandpa class");
}
}
class Dad extends Grandpa {
void show()
{
System.out.println("Inside show() method of Dad class");
}
}
class Me extends Dad {
void show()
{
System.out.println("Inside show() method of Me class");
}
}
class GFG {
public static void main(String[] args)
{
Grandpa grandpa = new Grandpa();
Grandpa dad = new Dad();
Grandpa me = new Me();
grandpa.show();
dad.show();
me.show();
}} 
```

## Practical No. 3
#### Aim: - Demonstrate the concept of Abstract classes and Methods And Interface.
###### A) write a program to implement the concept of abstract classes and methods.

```
abstract class Animal {
abstract void makeSound();
 public void eat() {
 System.out.println("Concrete method in Abstract class");
 } }
class Dog extends Animal {
 public void makeSound() {
System.out.println("Abstract method");
 } }
class Main {
public static void main(String[] args) {
Dog d1 = new Dog();
d1.makeSound();
d1.eat();
 }
}

```
## Practical No. 3
###### B) Write a program to implement the concept of interfaces.

interface interface In1 {
final int a = 10;
void display();
}
class TestClass implements In1 {
public void display(){
System.out.println("Geek");
}
public static void main(String[] args)
{
TestClass t = new TestClass(); t.display();
System.out.println(a);
}} 

## Practical No. 4
#### Aim :-Demonstration to raise built-in exceptions and User Defined Exceptions
###### A)Write a Java program that takes two integer inputs from the user,representing a dividend and a divisor. The program should then perform the division operation and display the result. However, it should also handle arithmetic errors such as division by zero.


```
import java.util.Scanner;
class DivisionProgram{
public static void main(String args[]) {
Scanner sc = new Scanner(System.in);
int a, b, res;
System.out.println("Enter two numbers:");
a = sc.nextInt();
b = sc.nextInt();
 try {
 res = a / b;
 System.out.println("Result = " + res);
 } catch (ArithmeticException ae) {
 System.out.println("Exception has occurred. You have entered the divisor as zero");
 } }}
```

## Practical No. 4  
###### B) Write a program to accept and display the month number throws an exception if improper month number is entered make your own exception class to handle this exception.

```
import java.util.*;
class MonthNumberException extends Exception {
MonthNumberException(String str)
{
System.out.println(str);
}
} class Month{
public static void main(String[]args)
{ int m;
Scanner sc=new Scanner(System.in);
System.out.println("Enter a Month number :");
m=sc.nextInt();
try {
if(m>12||m<1)
{
throw new MonthNumberException("Invalid month number"); }
System.out.println("Month Number Entered is " + m);
}
catch(MonthNumberException me)
{
System.out.println("Exception has Occurred");
} } } 
```

## Practical No. 5
#### Aim: - Demonstration for the concept of multithreading.

```
class OddNumbers extends Thread
{
public void run()
{
int i;
for(i=1;i<=10;i+=2)
{
System.out.println(i);
}
}
}
class EvenNumbers extends Thread
{
public void run()
{
int i;
for(i=2;i<=10;i+=2)
{
System.out.println(i);
}
}
}
class my
{
public static void main(String []args)
{
OddNumbers n = new OddNumbers();
Thread t1 = new Thread(n);
EvenNumbers n1 = new EvenNumbers();
Thread t2 = new Thread(n1);
t1.start();
t2.start();
}
}
```

## Practical No. 6
#### AIM :- Demonstration for Flow and Grid Layout.
###### A)Write a program to Demonstrate Flow Layout.
```
import java.awt.*;
class FlowLayoutDemo extends Frame {
public FlowLayoutDemo() {
FlowLayout fl = new FlowLayout();
setLayout(fl);
Label l1 = new Label("Enter User ID:");
Checkbox ch1 = new Checkbox("Pizza");
TextField tf1 = new TextField("This is textbox");
Label l2 = new Label("Enter Password:");
add(l1);
add(ch1);
add(tf1);
add(l2); }
public static void main(String ar[]) {
FlowLayoutDemo fr = new FlowLayoutDemo();
fr.setTitle(" Demonstrating FlowLayout");
fr.setSize(300, 300);
fr.setVisible(true);
} }
```
## Practical No. 6
###### B) Demonstrate Grid Layout and write a program to create a mobile keypad.
```
import java.awt.*;
class GridLayoutDemo extends Frame
{
GridLayoutDemo()
{
setFont(new Font("SansSerif", Font.BOLD, 24));
GridLayout gl = new GridLayout(4,3);
setLayout(gl);
for(int i=1;i<=9;i++)
{
add(new Button("" + i));
}
Button bt1 = new Button("*");
Button bt2 = new Button("0");
Button bt3 = new Button("#");
add(bt1);
add(bt2);
add(bt3); }
public static void main(String[]args)
{
GridLayoutDemo fr = new GridLayoutDemo();
fr.setTitle(" Demonstrating BorderLayout");
fr.setSize(300,300);
fr.setVisible(true);
}
}
```

## Practical No. 7
#### AIM :- Demonstration for MouseEvent and KeyEvent.
###### A)Write a program to demonstrate MouseEvent.
```
import java.awt.*;
import java.awt.event.*;
class MouseListenerDemo extends Frame implements MouseListener
{
String st = " ";
public MouseListenerDemo()
{
addMouseListener(this);
}
public void mouseClicked(MouseEvent me)
{
st = "Mouse is clicked";
showStatus(st);
}
public void mouseEntered (MouseEvent me)
{
st="Mouse Entered";
showStatus(st);
}
public void mouseExited(MouseEvent me)
{
st="Mouse Exited";
showStatus(st);
}
public void mousePressed(MouseEvent me)
{
st="Mouse Button Pressed";
showStatus(st);
}
public void mouseReleased(MouseEvent me)
{
st="Mouse Button Released";
showStatus(st);
}
private void showStatus(String st2) {
System.out.println(st2);
}
public static void main(String ar[])
{
MouseListenerDemo fr = new MouseListenerDemo();
fr.setTitle("Demonstrating MouseListener on Frame");
fr.setSize(300,300);
fr.setVisible(true);
}
}
```
## Practical No. 7
###### B) Write a program to demonstrate KeyEvent.
```
import java.awt.*;
import java.awt.event.*;
public class KeyListenerDemo extends Frame implements KeyListener
{
public KeyListenerDemo()
{
addKeyListener(this);
}
public void keyPressed(KeyEvent ke)
{
showStatus("Key Down");
}
public void keyReleased(KeyEvent ke)
{
showStatus("Key Up");
}
public void keyTyped(KeyEvent ke)
{
String st = "You typed: " + ke.getKeyChar();
showStatus(st);
}
private void showStatus(String str2) {
System.out.println(str2);
}
public static void main(String ar[])
{
KeyListenerDemo fr = new KeyListenerDemo();
fr.setTitle("Demonstrating KeyListener on Frame");
fr.setSize(300,300);
fr.setVisible(true);
}
} 
```