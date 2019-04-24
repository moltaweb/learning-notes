
# Java / Tim Buchalka

  

QUESTIONS

  

* Hello, I (think I) understand the concept of encapsulation and its benefits, but I'm a bit confused about the assertion Tim makes in the video, about the benefits of using getter/setter ratherthan accessing the variable directly.

we also need to change the name of the getter/setter

we can access the variable anyway

  

I mean in the end it's a matter of knowing what you're doing isnt'it?

  

* https://www.udemy.com/java-the-complete-java-developer-Course/learn/v4/questions/2331574

* https://www.udemy.com/java-the-complete-java-developer-course/learn/v4/questions/2224658

  

Monopoly:

* Tablero deberia ser un ArrayList de generico Casilla, pero habria que probar a hacerlo con y sin generico (video 115)

  
  

## TOC - Table of Contents

  

[1) Course Introduction](#1-course-introduction)

[2) Setup and First Steps](#2-Setup-and-First-Steps)

[3) Variables, Datatypes and Operators](#3-Variables-Datatypes-and-Operators)

[4) Java Tutorial: Expressions, Statements, Code Blocks, Methods and More](#4-Java-Tutorial-Expressions-Statements-Code-Blocks-Methods-and-More)

[5) Control Flow Statements](#5-Control-Flow-Statements)

[6) OOP 1: Classes, Constructors and Inheritance](#6-OOP-1-Classes,-Constructors-and-Inheritance)

[7) OOP Part 2](#7-OOP-Part-2)

[8) Arrays, Java Inbuilt Lists, Autoboxing and Unboxing](#8-Arrays,-Java-Inbuilt-Lists,-Autoboxing-and-Unboxing)

[9) Inner and Abstract Classes & Interfaces](#9-Inner-and-Abstract-Classes-&-Interfaces)

[10) GENERICS](#10-GENERICS)

[11) NAMING CONVENTIONS](#11-NAMING-CONVENTIONS)

[12) THE COLLECTIONS FRAMEWORK](#12-THE-COLLECTIONS-FRAMEWORK)

[13) JAVA FX](#13-JAVA-FX)

[14) BASIC INPUT & OUTPUT INCLUDING JAVA.UTIL](#14-BASIC-INPUT-&-OUTPUT-INCLUDING-JAVA.UTIL)

[15) CONCURRENCY IN JAVA](#15-CONCURRENCY-IN-JAVA)

[16) LAMBDA EXPRESSIONS](#16-LAMBDA-EXPRESSIONS)

[17) REGULAR EXPRESSIONS](#17-REGULAR-EXPRESSIONS)

[18) DEBUGGGING AND UNIT TESTING](#18-DEBUGGGING-AND-UNIT-TESTING)

[19) DATABASES](#19-DATABASES)

[20) JAVA NETWORKING PROGRAMMING](#20-JAVA-NETWORKING-PROGRAMMING)

[21) JAVA 9 MODULE SYSTEM](#21-JAVA-9-MODULE-SYSTEM)

  
  
  
  

________________________

## Section 1 -  

## 1) Course Introduction

  

```java

switch(variable) {
     
     
case value1:
          // code 1
          
// code 1

break;
     
case value2:  case value3:
          // code 2
          
// code 2

break;
     
case value4:
          // code 1
          
// code 1

break;

}

```

```java

// for loop

for(int i =  0; i<10; i++) {
     
// code
}
}

  

// while loop

while(condition) {
     
// code
     
// condition revision to avoid infinite loop
}
}

  

// do-while loop

do {
     
// code
     
// condition revision to avoid infinite loop

} while(condition) 

```

  

### Parsing values from a String

`  

```java

int number = Integer.parseInt(string);`

`double number = Double.parseDouble(string);`

```

  

(string must be a string that can be converted,for example 2018a does not work)


### READING USER INPUT  
  

### Reading user input

  

We use the built-in Scanner class (java.util)

  

```java

Scanner scanner =  new Scanner(System.in)

String input = scanner.nextLine();

scanner.close();

```

  

input numbers:

  

```java

// Option 1)

intinput = scanner.nextInt();

scanner.nextLine();          // we need this to allow to scan the Enter agter typing the int

  

// Option 2)

String input = scanner.nextLine();

int number = Integer.parseInt(input);

```

  
  

### Handling exceptions

  

We can add if-else for validation

Also methid scanner.hasNextInt() is a boolean that checks whether it's an integer

  

```java

boolean hasNextInt = scanner.hasNextInt();

  

if(hasNextInt) {
     
int input = scanner.nextIne();
     
scanner.nextLine();

     

// etc.

  

}

```

_____________________________


## Section 6 - OOP  

[Back to top](#toc---table-of-contents)

_____________________________

  

## 2) Setup and First Steps

  
  

### Overview of Software

  
  

### Which version of Java?

  
  

### First steps - Creating your first Java Program

  
  

[Back to top](#toc---table-of-contents)

_____________________________

  

## 3) Variables, Datatypes and Operators

  
  

### Your Programming Careers Questions Answered

  
  

[Back to top](#toc---table-of-contents)

_____________________________

  

## 4) Java Tutorial: Expressions, Statements, Code Blocks, Methods and More

  
  

[Back to top](#toc---table-of-contents)

_____________________________

  

## 5) Control Flow Statements

  
  

[Back to top](#toc---table-of-contents)

_____________________________

  
  

## 6) OOP 1: Classes, Constructors and Inheritance

  
  

### Classes

  

Objects in OOP have states and behaviors

  

* attributes

* methods

  

Classes are footprints for creating objects

  

A class could be seen as a powerful user-defined data-type (not exactly, but to give an idea)

  

To create a class:

  

```java

public  class ClassName {
    
// attributes + methods

}

```

  

This creates automatically a file `ClassName.java`

  

To instantiate:

```  

```java

ClassName myObject =  new ClassName();

```

  

As a general rules, in our user-defined classes, we will define internal variables as "private" (encapsulation)

We access these through getters/setters methods -> this is for encapsulation best practice
 Why? because this is more powerful, we can assdd validation, etc.


  
  

### Constructors

  

Constructors are special methods defined in the class. They are called when instantiagting an object (like __init__() in Python)

  

Now, constructors can be overloaded. Exmple:

  

```java

BankAccount acc1 =  new BankAccount();

// or

BankAccount acc1 =  new BankAccount("12345", 0.0, "Bob Smith", "bob@email.com", "+34612345678");

```

  

Even more, we can call one constructor forom another constructor. For example, when we call the empty constructor, this could call the overloaded constructor with some default parameters. Example inside the constructor definition:

  

```java

public BankAccount() {
    
this("00000", 0.0, "Empty name", "no-email", "no-phone");
}
}

```

  

This is optional, not mandatory. But beware, the this() line must be the first line inside the constructor method

  

Typically we will have a global constructor with all the parameters

Then the rest of conscuctors will call this one with this(a, b, c, d, e)

defaulting values. For example:

this("0000", 0.0, c, d, e) will default a and b

  
  

In the constructor, we have 2 options to initialize variables:

  

this.variable = variable;

or

setVariable(variable);

  

There are opinions for both. Tim prefers option1, general rule of thumb do not call other methods inside the constructor (except to call another constructor overload)

Because there migh tbe scenarios where the setter is not executed (we will see that)


  
  

### Inheritance

  

use keyword "extends"

  

A subclass inherits all data and methods from its super class

It can also override the methods from the super class: annotation @Override

  

To access methods and data from the superclass we use super.method() or super.data



  
  
  

### Reference vs Object vs Instance vs Class

  

Very good video, explains clearly references to objects

  
  

Class: the blueprint

Object = Instance: An instance of the class

Reference: The address of the object

  

Example:

Class: house plan

Object: house built

Reference=variable: The address of the house built

  

We can copy the reference as many times as we want, but there is only 1 house built

  

In Java we always have references to Objects in memory, we never access the object directly, only through the reference


  
  

### this vs super

  

Very good video, explains clearly

  

this: used to access/call the instance variables and methods. Required when we have a parameter with the same name, to distinguish both. Commonly used in constructors and setters

super: used to access/call the parent variables and methods

  

We can use them anywhere except on "static" areas

  

this(): used to call a constructor from another overloaded constructor in the same class. Can be used only in a constructor, and must be the first statement in the constructor

super(): used to call the parent constructor, and must be the first statement in the constructor

The Java Compiler puts a default call to super() if we don't add it

  

A constructor can call super() or this(), but not both


  
  

### Method overloading vs. overriding

  

Overloading:

	* 
  

* methods must have the same name

	* 
methods must have different parameters

	* 
May or may not

	* 
have different return types

	* 
have different access modifiers

	* 
throws different exceptions

	* 
Generally within same class (not necessarily)

  

Overriding:

	* 
define a method in a child class that already exists in the parent class with the same signature (name and arguments) 

	* 
also known as Runtime Polymorphism

	* 
Recommentadion to use annotation @OVerride

	* 
Cannot override final, static, private and constructor methods, only instance methods




  
  

### static vs instance

  

Static methods do not require an instance to be called (exple: System,out.println)

Instance methods require an instance created through the "new" keyword

  

static variables are shared among all the instances of a class. When we modify a static variable in one instance of a Class, its value is modified in all other instances

  

instance variables belong to the instance, each instance has its own copy of the variable


## Section 7 -  
  

[Back to top](#toc---table-of-contents)

_____________________

  

## 7) OOP Part 2

  
  

### Composition

  

Composition defines a relationship. Example: a Computer has a Motherbord, a Monitor, a Case

  

Inheritance is an "is-a" relationship. Composition is a "has-a". You do composition by having an instance of another class C as a field of your class, instead of extending C

  

This also allows ro concatenate method calls. Exple:

thePC.getMonitor().drawPixelAt(1500, 1200, "red");


  
  

### Encapsulation

  

Encapsulation in Java is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit. In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

  

The goal is not security, but to limit the functioning of classes to affect other classes. Thus, classes act as black-boxes.

  

We try and prevent possible issues: 

	* 
accessing private data that we might not want to expose

	* 
if we change the name of a variable in our class, if public, we must go and change it everywhere

	* 
assist data validation, through constructors and getters/setters




  
  

### Polymorphism

  

Polymorphism is the mechanism in OOP that allows actions to act differently based on the actual object that the action is begin performed on



ARRAYS, JAVA INBUILT LISTS, AUTOBOXING AND UNBOXING

  
  

[Back to top](#toc---table-of-contents)

______________

  

## 8) Arrays, Java Inbuilt Lists, Autoboxing and Unboxing

  

### Arrays

  

Data structure allowing to store multiple values of the same type (primitive) into a same variable of pre-known size

  

2 ways to create an array:

  

1. Direct

  

```java

int[] myArray = {0,1,2,3,4,5,6,7,8,9}     // array initiliazer block

```

  
  

2. Indirect

  

```java

int[] myarray =  new  int[10];    // create array and initialize elements to its default value (0 for int, null for String, etc.)

myArray[0] =  0;

myArray[1] =  1;

for(int i=0; i<10; i++) {
     
myArray[i] = i;

}

```

  
  
}



### Reference Types vs Value Types

  

All the primitive types (int, boolean, double...) are value types. They store values

  

Objects (Arrays, Strings...) are reference types. They store references to objects

  

Primitive variables hold an address in memory in which a value is stored. New copies create new locations in memories, indepenendet, each with their own value

  

A reference works differently, it holds a reference to an object, but not the object itself.

If we create a copy of the variable and modify the object, the original is also modified

As a rule of thumb, only the "new" keyword creates an object. The rest are only references to the original object



  
  

### List and ArrayList

  

List is an interface that extends interface Collection

The ArrayList class implements List

ArrayList is similar to an array, it's a sequence of ordered elements of the same type, but it's resizable

  

To define it:

  

```java

private  ArrayList<String> groceryList =  new  ArrayList<String>();

```

  

Between <> we put the type of contents in the list (it can hold objects). The final () is because it's a class, and therefore has a contructor (here empty)

  

To add elements
: `groceryList.add(item);`

  

Useful methods:

	* 
add(item) - append to the list

	* 
size() - equivalent to array.length

	* 
get(item) - read

	* 
set(position, item) - append in a given position, also replaces existing item

	* 
remove(position)

	* 
contains(item) - search element in the list, returns boolean

	* 
indexOf(item) - search element in the list, returns index position (-1 if not)

	* 
toArray(array) - convert list to array

  
  

To duplicate an ArrayList, 2 similar options:

  

	1. 
create + add

  

```java

ArrayList<String> newArray =  new  ArrayList<String>();

newArray.addAll(groceryList.getGroceryList());


	1. 
```

  

2. create instantiating

  

```java

ArrayList<String> newArray =  new  ArrayList<String>(groceryList.getGroceryList());

```

  
  

Project implementation


	1. 
  

* create a class GroceryList



	1. 
declare a new ArrayList private within the class

	2. 
create methods for



	12. 
add itemto the list -> .add()

	2. 
print all items in the list -> .get() (via .size())

	3. 
update an item in the list -> .set()

	4. 
delete an item from the list -> .remove()

	5. 
find an item in the list -> .indexOf()



	* 
create a class Main



	1. 
variables



	1. 
* scanner

	2. 
* groceryList = new GroceryList();



	* 
2. methods



	1. 
* main



	1. 
display menu

	2. 
scanner int for choice

	3. 
swicth case options menu



	* 
printInstructions

	* 
addItem



	1. 
scanner item

	2. 
call groceryList.addItem



	* 
modifyItem



	1. 
scanner position

	2. 
scanner new ite

	3. 
call groceryList.modifyItem



	* 
* removeItem



	1. 
scanner position

	2. 
call groceryList.removeItem



	* 
searchItem



	1. 
scanner item

	2. 
call findItem




  
  
  

### Autoboxing and Unboxing

  

We can use primitives as objects by using their wrapper classes:

	* 
  

* Integer

	* 
Double

	* 
Float

	* 
etc

  

Autoboxing means converting a primitive to an object

Unboxing means retrieveing the primitive value from the object wrapper

  

This allows us, among other things, to use wrapper classes in an ArrayList, becaus AL only accepts objects, not primitives

  

Technically we should do:

  

```java

// Autoboxing

Integer myIntValue =  new Integer(54);

// or

myIntValue = Integer.valueOf(54);

And u  

// Unboxing:

int myInt = myIntValue.intValue();


  

// But Java let's us do a shortcut:

Integer myIntValue =  54;

int myInt = myIntValue;


```

  
  

### LinkedLists

  

Similar to an ArrayList, but better optimized in memory management for large reacords

Each item stores 2 things:

	  

* the value of the item
	
* a link that points to the next item

  
  

In an ArrayList, elementos are stored in memory subsequently, so each time we insert a new item, later items have to move down. If we remove an ite, they have to move up. When we have millions of records, this can be quite consuming

  

Simply put:

	  

* use ArrayList when we do not need to insert/remove a lot, but rater read/update (get/set)
	
* use LinkedList when we need to rearrange a lot (add/remove)




  
  

> NOTE
: another way to iterate through a list (equivalent to a for loop)

  

```java

Iterator<String> i = linkedList.iterator();

while(i.hasNext()) {
    
System.out.println(i.next());

}




INNER AND ABSTRACT CLASSES & INTERFACES

```

  
  

[Back to top](#toc---table-of-contents)

____________

  

## 9) Inner and Abstract Classes & Interfaces

  
  

### Interfaces

  

An interface specifies methods that the class that implements the interface must define

The interface is abstract; it does not have any code, just themethod names and parameters

  

It s usally started with an I, but maybe not anymore these days. It was done so for easy identification, but now with IDEs its not hat useful and adds bluff

  

It can be seen as a contract, a commitment on what signature the class methods will have. This is useful in large projects or frameworks, because we know we can use certain methods and thos will not change.

  

How to define an interface:

  

```java

public  interface ITelephone {
     
     
public  void dial(int phoneNumber);
     
public  boolean isRinging;
     
public  void callPhone(int phoneNumber);

}  

}

```

  

By convention, interface names start with I

Actually the access modifiers are redundant

  

How to define a class that implements an interface:

  

```java

public  class MobilePhone implements ITelephone {

     

@Override
     
public  void dial(int phoneNumber) {
          // code
     }

}

// code

}

  

}

```

  

Finally, to use and instantiate:

  

```java

ITelephone myPhone;

myPhone =  new MobilePhone();

```

  

We can declare the object using the type of the interface, or the class type

But we cannot instiate the interface directly:

  

```java

// This is not allowed

ITelephone myPhone =  new ITelephone();
Is not allowed

```

  
  

Notes

	*  

> It's a good habit, for example when we work with lists, to declare our variables as the interface (ie, List) and then apply one type or another when we instantiate
	* 
		* 
  

Example:

  

```java

List myList;

// and then

myList =  new  ArrayList<Object>;

// or

myList =  new  LinkedList<Object>;


	*```

  

> Sometimes it can be difficult to decide wheter to create a Class as a subclass (inheritance) or as an implementation (interfaces). 
	* 
		* 

  

Good rule can be if the new class "is-a" or "has-a". for example a MobilePhone could be a subclass of Phone. But a MobilePhone hasmore things besides phone capabilities(also computer, video, apps, etc.. DeskPhone is also a phone. So best approach is they both implement the IPhone interface
		* 
  

also remember Java only allows 1 single inheritance. So to "inherit" from multiple classes we have to use interfaces




  
  

### Inner Classes

  

In Java it's possible to nest classes inside other classes. We have to write them at the end, after attributes and methods

  

There are 4 types of inner classes:

	* 
  

* static nested (mainly used to associate a class with an outer class)

	* 
non-static nested (inner)

	* 
local (inner defined inside of a scope, a method)

	* 
anonymous (nested without a class name)




  
  

#### Inner classes (non-static)

  

They make sense to define a class that is not relevant out of certain context. For example, we could define a Gear class inside a Gearbox class. Other code may want to acces the Gearbox class, but Gear is something internal to Gearbox

  

Instantiation:

  

```java

Gearbox mcLaren =  new Gearbox(6);

Gearbox.Gear first = mcLaren.new Gear(1, 12.3);

```

  

TO BE CONTINUED



  
  
  

### Abstract classes

  

Classes that implement method signature only. They cannot be instantiated, only nherited by other subClasses (that can themselves be instantiated)

  

If the subclass does not implement all the methods of the parent class, it must also be declared abstract


  
  

**Abstract class vs. Interface**

	* 
Interfaces are 100% abstract, AC can have some abstract methods and some aren't + can have attrbitutes

	* 
What is the relationship between our classes. "Is a" (inheritance) vs "can" (interface) vs "has a" (interface)

	* 
AC can have member variables that can be inherited. Itfces can only have private static final variables (constants)

	* 
AC can have a constructor

	* 
Methods in Itfces are automatically public, whereas in AC they can have any visibility




  
  

### Interfaces



  
  
  

[Back to top](#toc---table-of-contents)

______________

  

## 10) GENERICS

  

### Generics introduction

  

We have already been using them. IT's the fact of assigning a type to a List. Example:

  

```java

ArrayList<Integer> items =  new  ArrayList<>();

```

  

The operator on the right is called "diamond". Here we specify that the AL will be storing Integers

  

This is also allowed for backwards compatibitiliyy (Generis were introduced in Java 5):

ArrayList items = new ArrayList();

But not recommended at all. The problem is the compiler will not say anything if we try to insert a String in the ArrayList, but after the code vcould assume it's only integers.

  

The goal is to try and spot errors in the code as early as possible in compile time


  
  

### Our Generics class

  

Generics allow to define a generic type for alist. For example in Monopoly:

  

```java

ArrayList<Casilla> tablero =  new  ArrayList<>();

```

  

But what if we wanted a tablero of only Propiedades?

  

Let's see an example with Players and Teams

  

```java

// we define the class to accept any Type that extends Player

public  class Team<T  extends  Player> {
    
// code
    
private  ArrayList<T> members =  new  ArrayList<>();

}

```

  

The first player we add to the team will specify the type contained in the ArrayList

  

Player can either be a class or an interface. Even multiple interfaces with '&':

  

```java

public  class Team<T  extends  Player & Coach & Manager> {




```

  
  

[Back to top](#toc---table-of-contents)

_______________

  

## 11) NAMING CONVENTIONS


  
  

### Naming conventions


	*   

Packages

	* 
lower case

	* 
unique names

	* 
use internet domain name reversed

	*   

Classes

	* 
CamelCase, start with capital letter

	* 
should be nouns (they represent things)

	* 


	* 
Interfaces

	* 
CamelCase

	* 
should represent what the class is intended to be/do (List, Serializable, Coumpound...)

	*   

Methods

	* 
mixedCase

	* 
often verbs

	* 
Constants

	* 
UPPERCASE

	* 
separate words with underscore_

	*   

Variables

	* 
mixedCase

	* 
meaningful and indicative

	* 
No underscores

	*   

Type parameters

	* 
single characters

	* 
capital letters





  
  
  

### Packages

  

Allow the use of classes with same name in the same project

Packages are a way of grouping related classes and interfaces together

  

We can use a class in an external package either by importing or by calling the full path in the variable declaration. 

But we can't import 2 classes named the same from different packages, only one. For the others we have to use the full path declaration.

  

Reasons for packages

	* 
Related classes and interfaces together

	* 
Each package creates a new namespace

	* 
Classes within a package have unrestricted access to one another while still restricting access for classes outside the package

  
  

To import everything from a package:
 `import path.to.package.*`

  

This imports all classes, interfaces and static objects, but not the subpackages. 

Ie:
 `path.to.package.subpackage
` Is another package.

  

Also, the package name must match de directory path.

  

To import a class:
 `import path.to.package.Class`


  
  

### Scope

  

The scope of variables is that of the nearest and most specific code block defined within { }

If defined in the class scope, it is available also in inner scopes

  

For example 2 variables named the same, one in the class the other in the method. In the method will be used the one defined wihin the method. If we want to refer to the one in the class we must use this.var

  

If we have inner classes, in order to distinguish between the myVar in innter class vs the one in the class si this.myVar is for innerclass and Class.this.myVar is for the one in the class


  
  

### Visibility

  

It is determined by the access modifiers

  

Between a class and its inner classes, everything is visible, even if marked as private


  
  

### Access modifiers

  

	* 
public: visible everywhere

	* 
private: only visible within the class, not even in subclasses

	* 
protected: visible only in the package, but also in sub-classes (even if they are in another package)

	* 
package-private (no keyword): visible only in the package (special case: in interfaces, all methods are public no matter the access modifier we put them. But of course, if the interface itself is not public, nothing will be visible outside the package)


  

	* 
Top level: only classes, enums and interfaces. Everything else must be included in one of these



	* 
public

	* 
package-private



	* 
Member level: 



	* 
public

	* 
package-private

	* 
private




  
  
  

### The '*static'* statement

  

A static method can be called directly through the class, not through an instance of it

  

A static property is shared by all the instances of the class. Otherwise, each property belongs to each object

For example: a global counter of instances

  

> Important: a non-static property/method cannot be accessed from a static context.



  
  

### The '*final'* keyword

  

The value of a property marked final cannot be changed after the class has been created or instantiated through a contrsuctor

A method declared as final cannot be overwritten in subclasses

  

Also, if static: constant por all the class: Math.pi. This is the typical usage of "final"

If not static, each instance has its own constant (Id for example)

  

When used in a class declaration, 'final' prevents the classed from being extended. Example:

public final class Math {}



  
  

### Static initializers

  

This is an advanced feature, rarely used. It's a means to create a constructor block in a static class. A code block that will execute the first time the class is loaded. Kind of a constructor for static classes, rather than for objects.

  

They go inside a static code block:
 `static {}`

  

There can be as many as we want. They are executed in order, first al lthe statics and then the rest of the code.



  
  
  

[Back to top](#toc---table-of-contents)

________________

  

## 12) THE COLLECTIONS FRAMEWORK

  

### Collections Overview




Binary Search





  
  
  
  

### Binary Search

  
  
  
  
  

### Collections List Methods




  
  
  
  

### Comparable and Comparator




Maps




  
  
  
  

### Maps

  
  
  
  

### Map Continued and Adventure Game




  
  
  
  

### Adding Exits to the Adventure Game




  
  
  
  

### Adventure Game Challenge




  
  
  
  

### Immutable Classes





Sets & HashSet









  
  
  
  
  

### Sets & HashSet

  
  
  
  

[Back to top](#toc---table-of-contents)

___________

  

## 13) JAVA FX

  
  

JavaFX can ce built either through Java code or through FXML.

  

Best practice is to do the UI through FXML as much as possible.

  

Layouts allowto manage automatically how the elements are displayed, the resizing of the window, preferred size for controls, etc.

  

JavaFX has 8 built-in layouts:

	1. 
GridPane

	2. 
AnchorPane

	3. 
StackPane

	4. 
HBox

	5. 
VBox

	6. 
FlowPane

	7. 
BorderPane

	8. 
TilePane

  

https://docs.oracle.com/javafx/2/layout/builtin_layouts.htm

  

But we can also create our custom layouts (advanced)

  

Tags

	* 
padding



	* 
InSets



	* 
columnConstraints



	* 
ColumnConstraints



	* 
Button



	* 
prefWidth



	* 
Label

	* 
GridPane

	* 
HBHox

	* 
VBox

	* 
* BorderPane



	* 
top

	* 
bottom

	* 
left

	* 
right

	* 
center





  
  

### GridPane layout

  

Elements are arranged in a grid composed of cells. Each cell will be as wide as its widest element and as tall as the tallest element it contains.

  

Similarly to grid pane in Tkinter, we set positions for each element:

  

```java

GridPane.rowIndex="2" GridPane.columnIndex="0"

```

  

Intersting feature for debugging, add this attribute in the GridPane element: 
`gridLinesVisible="true"`

  

We can use a class `<columnConstraints>` to set the width of columns, in px (absolute) or % (relative to the size of the window)


  
  

### HBox/VBox layout

  

HBox lays its children horizontally in a single row, and sets their width to their preferred width

  

Usually used in dialog windows or as a child of another layout

  

VBox is the same, but vertically


  
  

### Layouts

  

#### BorderPane layout

  

Very commonly used for client applications

  

It has 5 sections: top, left, center, right and bottom

We don't need to use them all


  

#### AnchorPane

  

Popular also, allows to anchor elements (for example: Title on the top)


  

#### FlowPane

  

Elements are like CSS-floated, they wrap each other depending on the size of the window

Similar to HBox or VBox, we whould use those when we don't want the elements to wrap

  

FlowPane is useful for example when we pop up items from DB and don't know how many beforehand


  

#### TtilePane

  

Very similar to FlowPane, except all cells have same size


  

#### StackPane

  

Occupies a single cell, all elements are stacked on top of each other (like z-index)


  
  
  

### Controls

  

https://docs.oracle.com/javafx/2/ui_controls/overview.htm

https://docs.oracle.com/javase/8/javafx/user-interface-tutorial/ui_controls.htm

https://www.oracle.com/technetwork/java/repository-140393.html


	* 
  
  

* Button - text



	* 
graphic



	* 
ImageView



	* 
Image - url



	* 
Label - text, textFill, WrapText



	* 
font



	* 
Font - name, size



	* 
graphic



	* 
RadioButton - selected

	* 
CheckBox

	* 
ToggleButton

	* 
TextField

	* 
PasswordField

	* 
ComboBox - editable

	* 
ChoiceBox (very similar to Combobox, normally not very used)

	* 
Slider - min, max, showTickLabels, showTickMarks, minorTickCount, snapToTicks

	* 
Spinner (available from Java 1.8u40) - min, max, editable, initialValue

	* 
ColorPicker

	* 
DatePicker

	* 
TitledPane (can be used standalone or within an Accordion)

	* 
Accordion



	* 
panes





  
  

### Events and event handlers

  

Procedural application vs event-driven

  

UI thread is waiting for user's interaction. Whenever the user does an action, the thread looks if any control is supposed to react to that action

  

As programmers, we have to write the event handlers. 

	* 
We write the methods in the Controller.java file 

	* 
we link actions in the FXML: onAction="#methodName"

  

On the other hand, we can also retrieve data frm the UI (for example a TextField) to treat it in the controller. To do so, we annotate @FXML the variable in the Controller, with the same name as in the Fxml

  

Also, we can add parameters to the controller method. 

For example, 2 buttons can call the same method -> ActionEvent can help determine the source

  

Finally, we can use the initialize() method to initialize the state of UI controls


  
  

### UI Thread

  

The UI thread sits and waits for the user to do something. And when the user does something, it checks whether the application is listening that event, and if so, it dispatches it to the concerned event handler.

Now the event handler itself also runs on the UI thread. So when an event handler is running, the UI thread is busy to listen to other events.

  

We have to make sure when programming that when we're processing things in our event handlers, we go back to the UI thread as quick as possible, otherwise we'll have a bad user experience.


  
  

### Threads and runnable

  

We will see more about threads in concurrency, but the main idea is that if we have to deal with a process that takes some time (>1s), we should open another thread to process it in the background and free our UI thread.

  

We can do that using the Runnable class and the Platform.runLater() method

  

We will se more in the concurrency section


  
  

### Setup sample ToDo list application



  
  

### Add change listener


	*   

Split the central part in to VBoxes: textarea and due date




  
  

### Singletons

  

	* 
singleton to store the data 

	* 
try-with-resources

	* 
basic IO to a file

	* 
observableArrayList





  
  
  

[Back to top](#toc---table-of-contents)

______________

  

## 14) BASIC INPUT & OUTPUT INCLUDING JAVA.UTIL

  

### Exceptions

  

There are 2 approaches for dealing with exceptions typically:

	  

* LBYL - Look Before You Leap
	
* EAFP - Easy To Ask for Forgiveness and Permission

  

In Java the approach is more LBYL. Example: check an object is not null before we approach it

  

```java

// Example LBYL:

if (y !=  0) {
    
return x/y;

} else {
    
return  0;

}

  

// Example EAFP:

try {
    
return x/y;

} catch(ArithmeticException e) {
    
return  0;
}
}

```

  

There's a lot of debate in to which approach is better. Both are good and better than none.

Depending on the scenario, LBYL can require much more code (example: input integer check not a string), but also can be quicker (check if a key exists in a map)


  
  

### Stack Trace and Call Stack

  

An "Exception" is an event that occurs during the execution of a program that disrupts the normal flow of the program's instructions.

--> something that goes wrong somewhere

  

Exceptions and RuntimeExceptions are classes defined in `java.lang`

All exceptions are subclasses of these two

  

We can catch the parent generic type, but it's better to be specific (ex: InputMismatchException) because the type of exception gives the information on what went wrong.

  

The call stack is a stack of all the method calls our program goes through. so when a method is called, it is stacked at the top of the stack, and when it returns, the method is removed form the stack.

So when we get an exception, at the top we have the method that has thrown the exception, so to retrieve the path it's best to start from bottom to top.

When an exception is thrown, the JRE goes through the call stack backwards (to the bottom of the stack) to see if any of the methods has been programmed to handle the exception, until it finds one that has. Only if there's not any, the program is interrupted and the JRE prints the stack trace.


  
  

### Catching and Throwing exceptions

  

As a general rule, it only makes sense to catch an exception if our code can do something useful with that. Example: request another input if we detect it's not an integer.

  

Advice: keep code in "catch" blocks as simple as possible, to avoid the odds of generating an exception also in the catch...

  

A possibility is to throw a new exception inside the catch block, this way we call the stack trace while keeping it simple:

throw new ArithmeticException("attempt to divide by 0");


  
  

### Multi-catch exceptions

  

We can concatenate several catches. If one is caught, then the exception is thrown and the others are not tempted:

  

```java

try {
    
x = getInt();
    
y = getInt();
    
return x / y;

} catch(NoSuchElementException e) {
    
throw  new ArithmeticException("no suitable input");

} catch(ArithmeticException e) {
    
throw  new ArithmeticException("attempt to divide by 0");

}

```

  

From Java 7 we can also combine catches:

  

```java

try {
    
x = getInt();
    
y = getInt();
    
return x / y;

} catch(NoSuchElementException | ArithmeticException e) {
    
throw  new ArithmeticException("unable to perform operation");
}
}

```

  

(NOTE it's a single pipe sign, not double)


  
  

### Introduction to I/O

  

There are various ways in Java to do I/O

Even a new library NIO introduced in Java 7

We will see the main mathods used, and discuss pros/cons

  

Input: reading data from a source (files, databases, pipes, network connections, keyboard...)

Output: writing data to some destination (files, databases, network connecitons, console, screen...)

  

I/O can be performed using either Byte or Character data. The methods used are pretty much the same, but the actual classes vary. Which one to use depends on the typeof data.

  

Another distinction is to be made:

	  

* serial/sequential files : stream of data IN or OUT of our program, in order with a predefined sequence
	
* randome access files : refers to files, allows to jump within the file to access some specific data. This is to work for example with a database in file format






















> Written with [StackEdit](https://stackedit.io/).  
  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 15) CONCURRENCY IN JAVA

  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 16) LAMBDA EXPRESSIONS

  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 17) REGULAR EXPRESSIONS

  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 18) DEBUGGGING AND UNIT TESTING

  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 19) DATABASES

  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 20) JAVA NETWORKING PROGRAMMING

  
  

[Back to top](#toc---table-of-contents)

_________________

  

## 21) JAVA 9 MODULE SYSTEM

  
  

[Back to top](#toc---table-of-contents)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMTcyNDQxMjUsLTEzNzc0NzQ2NzcsLT
IzNTM4MjAxNF19
-->