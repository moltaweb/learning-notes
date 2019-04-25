

## INTRODUCTION



_______________

## WHAT IS JAVA





_______________

## GET STARTED




_______________

## WORK WITH VARIABLES

### Work with Primitive values

In Java there are 2 types of data:
* primitives
* complex (classes)

Primitives are numbers, characters and booleans. They contain values, not objects

| Data Type | Bits | Minimum | Maximum
| --- | --- | --- | ---
| byte | 8 | -128 | 127
| short | 16 | -32,768 | 32,767
| int | 32 | -2^31 | 2^31-1
| long | 64 | -2^63 | 2^63-1
| float | 32 | see the docs | 
| double | 64 | see the docs |

We can extend the functionality of primitive values thanks to their Helper classes:

| Data Type | Helper Class |
| --- | --- |
| byte | Byte |
| short | Short |
| int | Integer |
| long | Long |
| float | Float |
| boolean | Boolean |
| char | Character |

For example they contain methods 
* to help casting between types
* to use unsigned integers to double the range of memory

Every class in Java contains the toString() method. In some cases it's not very useful, but for primitives for exple, it converts to a String object


### Declare and modify primitive values

To declare a variable:

`type varName = value`

Exple:  
byte b = 12;  
short s = 20000;

Helper classes contain attributes that tell us the max value possible:

Byte.MAX_VALUE
127

If we do 
b = 128
It will turn around in cycle and will get the minimum, which is -128 actually



### Store currency values with BigDecimal

Because of the precision of computers, currencies in float and double may be error

To avoid that, we use the class BigDecimal. It's a little convoluted:

1. double value


**COMPLETE**


### Convert values between numeric types

Widening types is straightforward:

```java
short sh = 100;
int i = sh;
// i = 100
```

Casting a type into a larger one is ok, but the opposite must be explicit, because going from int to byte can cause losing data

```java
short sh = 1000;
byte b = (byte)sh;
```


### Math operators and the Math class

Basic operators: +, -, *, /

But note, if we do:

```java
int a = 56;
int b = 42;
int c = a/b;
// c = 1
```

Because c is type int (no decimals). We would need to declare double or float

Additionally, we can work with the Math class to have more operations. All methods in the class are static, which means we can call them directly from the class, no need to initiate an instance

Example methods of Math:
* round()
* abs()


### Work with boolean values

* true
* false


### Work with character values

`type char`

Literals are declared in ' '. 
For strings, it's " "

We can declare them with literals
`char c = 'a'`

or with their Unicode code:
`char dollar = '\u0024'`

We can use the helper class Character.   It has some useful methods:

* toUpperCase()
* toLowerCase()
* etc 

We can create an array of chars:

```java
char[] chars = {'a', 'b', 'c'}
```

and convert it to string :

```java
String s = new String(chars)
// "abc"
```

or reconvert it to array with the method from String:

```java
char[] chars2 = s.toCharArray();
```


### More about Java operators

Operators in Java are based from C, so we get the same we know already

Particularties
* variable ++; dsyplays variable and then sum 1
* ++ variable; sums 1 and then displays new
* instanceof, to determine if an object is an instance of a given class
* s1.equals(s2), to compare 2 strings s1 and s2 (equals is a method of String class), DO NOT USE == for strings
* ?=, Ternary operator. Example:

String message = i == 1 ? "There is 1" : "There are " + i;



_____________

## WORK WITH STRING VALUES


### Declare and initialize String objects

A String is a class, and strings are objects, instances of this class

We can create a string in 2 ways:
1. classic syntax

```java 
String string1 = new String("hello");  
```
2. special shortand for the String class

```java
String string2 = "hello";
```

Internally it's slightly different, but for most applications it's the same

Characteristics of Strings:
* a string is an array of chars (therefore we can loop them)
* String objects are immutable, once initialized, we cannot change them. If we modify a string, it creates a new direction in memory (like Python)


### Create and concatenate String values

3 ways to create a String:
1. String s1 = "This is a string";
2. String s2 = new String("This is a string");
3. String s3 = new String(chars);    // chars is an array of chars

method 1 is slightly different internally, we will see that later

To concatenate strings we can use the + operator

Some methods:
* toUpperString
* charAt - index of char
* getBytes - returns an arrayof bytes. Useful for streams
* format - similar to Python


### Convert primitive values to String

We can concatenate strings and primitives:

```java
int result = 20 + 12;
String answer = "The result is :" + result
// The result is 22";
```

Conversion happens automatically, as long as there is 1 string in the concatenation
If no string is present, we need to cast through helper classes:

```java
int intValue = 42;
String fromInt = Integer.toString(intValue);
// "42"
```

Note: we can use underscores to help redability, and internally they are removed

```java 
long longValue = 10_000_000;
// 10000000
```


### Build a string from multiple values

Everytime we create or modify a string, we reserve new space in memory (immutable objects)

To be more efficient, we can use the class StringBuilder and its append() method

This way, we append to the initial object and we are more effcient

```java
StringBuilder sb = new StringBuilder();
sb.append(text1);
sb.append(text2);
//etc.
```


### Compare String values with methods

We have seen different methods for creating Strings, they are not the same

```java
String s1 = "hello";
String s2 = "hello";

if (s1 == s2) {
    // true
} else {
    // false
}
```

> This is TRUE

```java
String s1 = new String("hello");
String s2 = new String("hello");

if (s1 == s2) {
    // true
} else {
    // false
}
```

> This is FALSE

Method 1 creates an identifier s1 pointing to a literal, and a second identifier s2 which will point to the same literal
Method 2 creates 2 separate objects.   
"==" compares equal values in the case of literals, and checks if same object in the case of objects

To truly compare strings, we must use the String.equals() method
(also available .equalsIgnoresCase() for case insensitivity)


### Format numeric values as strings

```java
class NumberFormat

double doubleValue = 1_234_567.89;
NumberFormat numberFormat = NumberFormat.getNumberInstance();
sysout(numberFormat.format(doubleValue);
>> 1,234,567.89
```

We call a methof format() of the created instance object

other methods:
* getIntegerInstance()
* setGroupingUsed(false)
* getCurrencyInstance()

Other classes:
* Locale
* DecimalFormat



### Parse String values

Useful methods on strings
* length()
* indexOf() - returns index of first element, -1 if None
* substring() - to extract
* trim() - to trim

Check the documentation
https://docs.oracle.com/javase/9/docs/api/java/lang/String.html



### Challenge: a simple calculator

```java
Scanner input = new Scanner(System.in);
             
System.out.println("Enter a first number: ");
String in1 = input.nextLine();
System.out.println("Enter a second number: ");
String in2 = input.nextLine();

double n1 = Double.parseDouble(in1);
double n2 = Double.parseDouble(in2);
double result = n1 + n2;

System.out.println("The sum of the two numbers is: " + result);
```            



___________________

## MANAGE PROGRAM FLOW

### Evaluate conditions with if-else

```java
if (condition) {
    // else
} else if {
    // code
} else {
    // code
}
```


### Evaluate conditions with switch-case

A more efficient alternative to if-else in some cases

```java
switch(condition) {
    case value1:
        // code
        break;
    case value2:
        // code
        break;
    case value3:
        // code
        break;
    default: 
        // code
}
```


### Create looping code blocks

```java
// For loop (iteration)
for(before;condition;after) {
     // code
}

// For loop (foreach)
for(type item : array){
    // code
}

// While loop
while(condition) {
     // code
}

// Do-while loop
do {
     // code
} while (condition)
```

At any time we can exit the loop wth the `break` keyword

Also available `continue`


### Create reusable code with methods

methods are functions or subroutines, inside a class
The `main` method is called from the CLI when we start up a class


### Create overloaded methods

In Java we can have several methods in a class with the same name, as long as each method accepts a different set of parameters (either in quantity or in type)

For example, we might want to create a function that acts differently depending on the arguments it receives

To pass an indefinite number of parameters:

```java
private static void myFunction(String... values) {
     // code
}
```


### Pass arguments by reference vs. value

**REVIEW**



### Challenge: a more complex calculator



_____________

## EXCEPTION HANDLING AND DEBUGGING

### Syntax errors vs. exceptions

2 types of errors in Java:
* syntax- errors that occur during compilation: in typing,missing semicolon, mispelling, incorrect keywords, etc.
* exceptions- errors that occur while the app is running

Examples of exceptions:
* out of index
* point to null value
* etc


### Debug with IntelliJ IDEA

Not applicable

### Handle exceptions with try-catch

Whenever we write code that could potentially throw an exception at runtime, we can wrap that code in a try-catch block

```java
try {
     // code with error
} catch(Exception e) {
     // code to treat the exception
}
```

Exceptions are instances of the Exception class

Also, we can try and catch exceptions individually per type:

```java
try {
     // code with error
} catch(ArrayIndexOutOfBoundsException e) {
     // code to treat the exception
}
```


### Create multiple catch blocks

```java
try {
     // code with error
} catch(ArrayIndexOutOfBoundsException e) {
     // code to treat the exception
} catch(NullPointerException e) {
     // code to treat the exception
} catch(Exception e) {
    // generic code
}
```


### Checked vs. unchecked exceptions

There are 2 types of exceptions:
* unchecked - no need to be declared
* checked - they need to be declares

Null pointer and Out of index are unchecked exceptions. They inherit from the RuntimeException class.

An example of unchecked is InterruptedException, we must declare it, either with a try-catch block, or with `throws` keyword

**REVIEW**



_________________

## CREATE CUSTOM CLASSES

### About encapsulation

Encapsulation is the logic of grouping the code into smaller pieces and put functions in their relevant classes

Methods pertain to their classes and are mostly hidden to users


### Use the Java runtime classes

To be completed

### Wrap code in static methods

Methods in Java are the equivalent to functions or subroutines in other languages. They are always defined into classes

Example to define a method:

```java
public static void main(String[] args) {
}
```

* main - the name of the method. Camelcase with start in lowercase
* void - return type, mandatory can be any type (String, int, void, etc...)
* static
    * static - the method can be called directly from the class, without need to first instantiate an object from the class
	* Else: instance
* public - visibility. Can be
	* public- visible in the entire application (also in other packages)
	* private - visible only in the class
	* protected
	* [none] - visible in the class and in other classes in the same package of the application


### Declare and use custom classes

Not only can we organize the code into methods within a class, but also across different classes

```java
public static class ClassName {
}
```


### Organize code with packages

Yet another tool to organize our code

A package is both:
* a description of where the class is in the application
* a description of where the class file is in the filesystem

We shall use reversed domain notation, for example:
`com.almis.awe.collat.DailyProgram`

We can also organize within subpackages inside an application

> Note: this doesn't affect the code, just file organization in folders (of course, the package path must be correctly imported)


### Create and use instance methods

As opposite to static classes, instance methods refer to data persistent to a particular object (class instance)

For that, just remove the keyword "static" from the method definition

Then, instead of calling the method from the class, like:
`Math.round();`

We call it from the object:

```java
String s = "hello";
s.length();
```

If the job can be done with static classes, it's better to use static because creating an object always consumes memory.  
But most times, we need to instantiate because the object will have its particular data, state, etc.


### Manage state with instance variables

Variables inside methods are local variables to the method

In a non-static class, when we declare a variable inside the class but outside of a method, that's an instance class

We can declare the variabe private and access it through setter and getter methods

Furthermore, without a setter, we can have a read-only variable


### Declare multiple constructor methods

Every class must have a construtor method. It's a special method that is called during instantiationt must have the same name  the class

But we don't need to define the method explicitly, if we don't create it, the compiler will do it for us

We can override the behaviour of the constructor method

```java
public NameOfClass() {
}
```

We can even overload the method (each declaration must have different parameters


### Use static fields as constants

In Java we declare constants with "static" and "final"Optionally, "public"

By convention, name of constants are UPPERCASE


### Declare and use enum types

Java supports a special type o values: *enum* (enumeration)It's a list of mutually exclusive values that are unique

We define it:

```java
public enum Operation {
    ADD, SUBTRACT, MULTIPLY, DIVIDE:
}
```

Then we declare/use it:

Operation option = ADD;


### Organize code with nested types

W can define the enumeration inide its own class


_____________

## WORK WITH INHERITANCE

### About inheritance and polymorphism

#### Inheritance

* Defines relationship between classes
* Java supports single inheritance: Each class can extend only one direct superclass (easier to debug)
* However, Classes can implement multiple interfaces

We call them superclass/subclass

Every class inherits from the class *Object*. Superclasses don't need a special code, they derive automatically from Object

If a class isnt' final, it can be extended. Fields and methods are inherited, unles they are marked as private

We can still make the data accessible with getter/setter methods

Example of subclass definition:

```java
public class Hat extends CLothingItem {
    @Override
    public String getType() {
        return "Hat";
    }
}
```

The getType() method from the superclass is overriden

We use an annotation *@Override* to improve readability and help the compiler catch errors (for exple the return type of the method)


#### Polymorphism

* Address an object as either a super or sub type
* Call inherited methods wthout knowing exact type
* Methods declare arguments as super type
* You can pass instances of sub types
* Improves code flexibility and reusability

Example:

```java
Clothing item = new Hat();
Sysout("This is a " + item.getType());
// Returns "Hat"
```


### Extend classes and override methods

In Java each class can inherit from only 1 superclass. If we create a class without the word "extends", it inherits from the Object class automatically

In this video we see an example of inheritance in a model ClothingItem / Shirt


### Cast objects as different types

A little complicated, we see polymorphism, and upcasting/downcasting between a class an its superclass

Also, we see the getClass() method to retrieve the class of an object


### Create and implement interfaces

In OOP, an interface is like a contract. It declares some methods and attributes that all classes implementing the Interface must have, but without actually defining them

```java
public interface Product {
    String getType();
    String getSize();
    int getPrice();
}
```

and then we call the extension

```java
public class CLothingItem implements Product {}
```


### Use abstract classes and methods

In addition to using interfaces we can create abstract classes

An abstract class cannot be instantiated directly, we can only instantiate their subclasses

```java
public abstract class CLothingItem implements Product {}
```


___________

## MANAGE DATA COLLECTIONS


### Store values in simple arrays

Java offers many ways to store collections of data

Typically we distinguish:
* ordered or unordered
* lists or dictionaries

The easiest way to store a list of ordered items is an Array
* index starts at 0
* cannot be resized after they are created
* all elements must be of the same type

We can create arrays in several ways:

```java
type[] carName = {item1, item2, item3};
```

Also, we can create the array but initialize it later:

```java
type[] varName = new type[3];
varname[0] = value0;
```

By default, non-initialised items will have a value of null

If we copy the array:

```java
type[] array2 = Arrays.copyOf(array1); 
```

We will have 2 arrays, but they point to the same objects. If I modify array1[1], array2[1] will also be modified



### Manage resizable arrays with List

The Java Collections framework is a set of classes and interfacees that help us work with sets of data
https://docs.oracle.com/javase/9/docs/api/java/util/doc-files/coll-overview.html


| Interface | Hash Table | Resizable Array | Balanced Tree | Linked List | Has Table + Linked List 
| --- | --- | --- | --- | --- | --- |
| Set | [HashSet](https://docs.oracle.com/javase/9/docs/api/java/util/HashSet.html) | --- | [TreeSet](https://docs.oracle.com/javase/9/docs/api/java/util/TreeSet.html) | --- | [LinkedHashSet](https://docs.oracle.com/javase/9/docs/api/java/util/LinkedHashSet.html) |
| List | --- | [ArrayList](https://docs.oracle.com/javase/9/docs/api/java/util/ArrayList.html) | --- | [LinkedList](https://docs.oracle.com/javase/9/docs/api/java/util/LinkedList.html)| --- |
| Deque | --- | [ArrayDeque](https://docs.oracle.com/javase/9/docs/api/java/util/ArrayDeque.html) | --- | [LinkedList](https://docs.oracle.com/javase/9/docs/api/java/util/LinkedList.html) | --- |
| Map | [HashMap](https://docs.oracle.com/javase/9/docs/api/java/util/HashMap.html) | --- | [TreeMap](https://docs.oracle.com/javase/9/docs/api/java/util/TreeMap.html) | --- | [LinkedHashMap](https://docs.oracle.com/javase/9/docs/api/java/util/LinkedHashMap.html) |

These classes implement interfaces (column 1). These interfaces declare the methods for adding, removing, etc

Their types are in the form of

`Interface<type>`

Here the type is a `generics <>`, where type must be an object (no primitives). For example, a list of integers would be done with the Helper class:

```java
List<Integer> ints = new ArrayList<>();
```

We can add items to the list with add()

Methods:
* add()
* remove()
* indexOf()


### Manage key-value pairs with Map

HashMap allows to define an unordered collection of key/value pairs (like the Python's dict)

```java
Map<String, String> map = new HashMap<>();
```

We declare the types of both the key and the value (not like Python)

map.put("California", "Sacramento");
map.put("Oregon", "Seattle");

https://docs.oracle.com/javase/9/docs/api/java/util/Map.html



________

## USE JAVA PACKAGES AND LIBRARIES

### Work with dates and times

There are 2 different modules in Java:
* java.util, the classic one
* java.time, new one from Java 8

```java 
Date now = new Date();
GregorianCalendar gc = new GregorianCalendar(2009, 1, 20);
DateFormat
```

NEW

```java
LocalDateTime ldt = LocalDateTime.now();
DateTimeFormatter dtf = DateTimeFormatter.ofPattern("M/d/yyyy");
```

> Look at the documentation



### Copy files with readers and buffers

Same as for datetimes, the I/O library has been reviewed in JE 7

Here we see a method common to old versions, including Android

```java
package com.example.java;

import java.io;

public class Main {

    public static void main(String[] args) {

        String sourceFile = "files/source.txt";
        String targetFile = "files/target.txt";

        try (FileReader fileReader = new FileReader(sourceFile);
            BufferedReader bufferedReader = new BufferedReader(fileReader);
            FileWriter writer = new FileWriter(targetFile);
        ) {
            while (true) {
                String line = bufferedReader.readLine();
                if (line == null) {
                    break
                }
                writer.write(line + "\n");
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

By putting the buffers in the "try!, we don't have to close them in the end, it is done automatically


### Copy files with Path and Files

The new nio module is more simple

```java
package com.example.java;

import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.nio.file.StandardCopyOption;

public class Main {

	public static void main (String[] args) {
		
		Path sourceFile = Paths.get("files", "source.txt");
		Path targetFile = Paths.get("files", "target.txt");

		try {
			Files.copy(sourceFile, targetFile, StandardCopyOption.REPLACE_EXISTING);
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
}
```

### Parse a JSON file

A JSON parser is not part of the Java Core. 
But there are a number of 3rd party libraries. One of them is Google GSON, available at Maven Central

The video exlains how to add a library in IntelliJ Idea

The how to use the Gson library

```java
package com.example.java;

import com.example.java.model.Flower;
import com.google.gson.Gson;
import com.google.gson.stream.JsonReader;

import java.io.FileReader;
import java.io.IOException;

public class Main {

	public static void main (String[] args) throws IOException {
		
		String fileName = "files/data.json";

		Gson gson = new Gson();
		try (FileReader fileReader = new FileReader(fileName);
			JsonReader reader = new JsonReader(fileReader) ) {
				Flower[] data = gson.fromJson(reader, Flower[].class);
				for (Flower flower : data) {
					System.out.println(flower);
				}
		}
	}
}
```

This is the power of encapsulation, all we need to know is how to instantiate the classes in Gson


### Include packages with modules

This video explains how to explicitly include a module in IDEA  
Modules are parts of packages  
Here we see an exple of a module to get Http Requests (module in Java 9 at the time of the video, now surely in the Core)

```java
import jdk.incubator.http.HttpRequest;
import jdk.incubator.http.HttpResponse;

import java.io.IOException;
import java.net.URI;
import java.net.URISyntaxException;

public class Main {

	private static final String DATA_URL = "http://domain.com/feeds/file.json";
	
	public static void main (String[] args) throws URISyntaxException, IOException, InterruptedException {
	
		HttpClient client = HttpClient.newHttpClient();
		HttpRequest request = HttpRequest.newBuilder()
										.uri(new URI(DATA_URL))
										.GET()
										.build();
		HttpResponse<String> response = client.send(request, HttpResponse.BodyHandler.asString());
		System.out.println(response.body());
	}
}
```


________________

## PREPARE A JAVA APPLICATION FOR DEPLOYMENT

### Document code with Javadoc

It's a tool included in the Core, to help us build documentation
we can wrap doc in special comment for /** .... */

We add this comments 1 line above the definition of the classes

Javadoc generates automatically documentation files in HTML formt (similar to the java doc in Oracle's website)


### Package classes in JAR files

Explains how to do it with IDEA
We create JAR files wth the "jar" tool
After, Jar files can be easily distributed and run in other systems
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDI5NTQ0Nl19
-->