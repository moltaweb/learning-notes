questions

* what if no @override? it also works the same, so what's the advatnage
* Coach theCoach = context.getBean("mycoach", Coach.class); - por que le pasamos los 2? con el id no es suficiente?
* method 2 annotations: what'se the point? its in the middle with both disadvantages
* method 3: scope and lifecycle?
* 148: why the validation is displayes in processFor


____________________________

## COURSE INTRODUCTION

### Introduction

Spring and Hibernate are very demanded skills for Java developers


### Practice Activities

It is highly recommended to do all the practice activities and homework on our own. This is the best way to learn


### How to take this course

Some students will watch the video first and then replay it while typing in the code. Others like to type along on the first watch. Choose whatever approach works for you.


### Downloading source code and PDF files

**Download Source Code:**

This only includes the source files, no JAR files. You will need to add JAR files separately on your own.

[http://www.luv2code.com/downloads/udemy-spring-hibernate/spring-hibernate-source-code-v26.zip](http://www.luv2code.com/downloads/udemy-spring-hibernate/spring-hibernate-source-code-v26.zip)

**Download PDF Files**

All slides which are shown during the course are available also as a reference and can be downloaded here:  
[http://www.luv2code.com/download-spring-hibernate-pdfs](http://www.luv2code.com/download-spring-hibernate-pdfs)


____________________________

## SPRING OVERVIEW





____________________________

## SETTING UP YOUR DEVELOPMENT ENVIRONMENT

### Downloading Spring 5 JAR files - Installation

1. Select latest version of Spring at https://repo.spring.io/release/org/springframework/spring/
2. Download the "dist" file
3. Open New Java Project (plain Java) in Eclipse
4. Create new folder "lib"
5. In the downloaded zip, copy all the jar files in the "lib" folder
6. Paste in "lib" in Eclipse
7. Right click on the project > Properties > Java Build Path > Libraries
8. Add JARs and select (CTRL SHIFT) all the jar files in lib
9. Ok. Now they are added to the project runtime


__________________________

## SPRING INVERSION OF CONTROL - XML CONFIGURATION

### What is Inversion of Control?

IoC is the buzzword we always hear when we talk about Spring.  
It's simply the design process of externalizing the construction and management of our objects. The creation of objects will be outsourced to an object factory.

It's passing an XML config file where we define the beans (objects that the factory container instantiates at runtime)


### Code Demo

We'll see an example through code: BaseBall coach + other sports

Requirement: 
* handle different types of coaches/sports
* app should be configurable

To make it configurable, it would be great if we had a simple config file that we could use rather than hard code the object implementations


### Spring IoC - Overview

Primary functions of Spring framework
* Create and manage objects (Inversion of Control)
* Inject object's dependencies (Dependency Injection)

There are 3 ways of configuring the Spring container:
1. XML configuration file (legacy, but most legacy apps still use this)
2. Java Annotations (modern)
3. Java Code (modern)

Spring Development Process
1. configure Spring Beans
2. create a Spring container (known as ApplicationContext)
3. retrieve Beans from Spring container


________________

## 5 - SPRING DEPENDENCY INJECTION - XML CONFIGURATION

### Spring DI - Overview

There are many types of injection in Spring. The 2 most common:
* Constructor Injection
* Setter Injection

> injection = helper

Injection it's just the fact that when we do a getBean(), we get it with all its dependent objects already instantiated (we will talk about autowiring in the annotations section later)

**Constructor injection. steps:**

1. define the dependency interface and class
2. create a constructor in your class that accepts the injections
3. configure the DI in the Spring config file `<constructor-arg>`


### Setter Injection - Overview

Spring will inject dependencies by calling setter methods from our classes

Steps

1. create setter methods in our class for injections
2. configure the DI in Spring config file `<property name>`

`<property name="nameOfTheProperty">`  
it expects to find a setter: `setNameOfTheProperty()`


### Setter Injection - Injecting literal values

We can also inject literal values in the XML  
`<property name="emailAddress" value="hello@me.com">`


### Setter Injection - Injecting literal values from a Properties File

We can also import literal values from another file so we don't have to hard code them inside the XML applicationContext

Steps:

1. Create a Properties file
2. Load Properties file in Spring config file
3. Reference values from the Properties file

We create a plain text file: myfile.properties  
and we type like in bash:
foo.email=myemail@mail.com
foo.team=My Sports Team

Then in the applicationContext file:
```xml
<context:property-placeholder location="classpath:myfile.properties">
<property name="emailAddress" value="${foo.email}">
```

Funny enough, it's like having a config file for the config file


_____________

## 6 - SPRING BEAN SCOPES AND LIFECYCLE

### Bean Scopes - Overview

Scope refers to the lifecycle of the bean
* how long does the bean live?
* how many instances are created?
* how is the bean shared?

The default scope is singleton
* The Spring Container creates only one instance of the bean
* It is cached in memory
* All requests for the bean will reference a same shared bean

Example:
```java
Coach alphaCoach = context.getBean("myCoach", Coach.class);
Coach betaCoach = context.getBean("myCoach", Coach.class);
```

These 2 refer to the same instance  
-> static instances

We can use the "scope" attribute to explicitly specify the scope:
* singleton - single shared instance
* propotype - new instance for each container request
* request - scoped to an http web request
* session - scoped to an http web session
* global-session - scoped to a global http web session


### Bean Scopes - Write some code

Singleton - same instance, same location in memory
Prototype - different instances and locations in memory


### Bean Lifecycle - Overview

This is the overall Spring process:
1. container starts
2. beans are instantiated
3. dependencies are injected
4. internal spring processing
5. Custom Init method
6. Application runtime until shutdown
7. Application is shutdown
8. Custom Destroy Method
9. Stop

In steps 5 and 8 we can define custom methods, typically we can use them to:
* call some custom business logic methods
* set up / clean up custom handles to resources (db, sockets, files, etc.)

We call them with attributes in the `<bean>` tag:
* init-method="myInitMethod"
* destroy-method="myDestroyMethod"

Steps:
1. Define methods for init and destroy
2. Configure the method names in Spring config file


Notes regarding init and destroy methods when using XML configuration:
* methods can have any access modifier (public, private, protected)
* methods can have any return type. However, we cannot capture any return value, so typically use "void" anyway
* methods cannot accept any arguments
* for prototype beans, the destroy method does not work (Spring does not manage the complete lifecycle of a prototype bean)


_________________

## 7 - SPRING CONFIGURATION WITH JAVA ANNOTATIONS - IoC

### Annotations Overview - Component Scanning

What are Java annotations?
* special markers added to Java classes
* provide meta data about the class
* processed at compile time or runtime

Why?
* XML can be very verbose (ie: when 30+ beans)
* Annotations minimize XML configuration

```java
@Component("myId")
```

Spring is going to scan our classes looking for annotations and when it find one, it register the beans from it with id "myId"

Development steps:
1. enable component scanning in Spring config file
2. add @Component to our classes
3. retrieve bean from Spring container


### Write some code

1) enable component scanning in Spring config file

add this tag:
```xml
<context:component-scan base-package="com.motlaweb.springdemo" />
```

2) Annotate the class
```java
@Component("theIdOfTheClass")
public class MyClassName {}
```

3) retrieve the bean
```java
Coach theCoach = context.getBean("theIdOfTheClass", Coach.class);
```

Overall, the Main class is the same, only difference is in the annotations in the classes, and no `<bean>` in the XML


### Default bean id

If we don't specify an id in the annotation, the default Id will be the name of the class with lower first letter:

```java
@Component
public class MyClassName {}
```

Here the id will be "myClassName"

EXCEPTION: when the className starts with 2+ capital letters. Exemple: RESTService
In this case, the default bean name remains the same (RESTService)


________________

## 8 - SPRING CONFIGURATION WITH JAVA ANNOTATIONS - DI

For DI with annotations, Spring uses Auto-wiring: 
* it looks for a class/interface that matches the property
* by scanning classes with @Component
* anyone implements the dependency interface?
* if so, it injects it automatically

With auto-wiring, there are 3 types of injections
* constructor
* setter
* field


### Constructor injection

Process
1. define the dependency interface and class
2. create a constructor in the class for injections
3. configure the dependency injection with @Autowired annotation in the constructor


### Setter injection

Inject dependencies by calling setter methods on the class

Process
1. define the dependency interface and class
2. create a setter method in the class for injections
3. configure the dependency injection with @Autowired annotation in the setter method

> NOTE: Actually we can use ANY METHOD with @Autowired, not necessarily a setter method


### Field injection

Inject dependencies by setting field values on your class directly (even private fields).   
This is accomplished using a technique named Java Reflection

Process
1. define the dependency interface and class
2. configure the dependency injection with Autowired applied directly to the field (no need for a setter method)

Spring autowires the field by instantiating afortuneService automatically


### Which Injection Type should we use?

Best advice is to choose a style and stay consistent throughout the project  
All 3 types provide same functionality


### Qualifiers for Dependency Injection

With @Autowiring, Spring automatically injects the bean. But what if there are multiple implementations of the same Dependency?

For example: HappyFortuneService, RandomFortuneService, BadFortuneService, LuckyFortuneService, etc. all with @Component

In such cases, we need to tell Spring which one to use. We do so with the @Qualifier annotation with its default bean Id (class name with small initial cap)  

This @Qualifier annotation can be applied to all cases
* constructor injection
* setter injection
* field injection

```java
@Autowired
@Qualifier("randomService")
private Fortune fortuneService;
```

> NOTE: for constructor method, the @Qualifier goes inside the argument:

```java
@Autowired
public TennisCoach(@Qualifier("randomFortuneService") FortuneService theFortuneService) {
	System.out.println(">> TennisCoach: inside constructor using @autowired and @qualifier");
        fortuneService = theFortuneService;
}
```


### Setter Injection with Annotations - Injecting literal values from a Properties File

We can also import literal values from the Properties file using Annotations

Steps
1. Create a Properties file
2. Load Properties file in Spring config file

```xml
<context:property-placeholder location="classpath:sport.properties"/>
```

3. Reference values from the Properties file

```java
@Value("${foo.email}")
private String email;

@Value("${foo.team}")
private String team;
```

We create a plain text file: myfile.properties and we type like in bash:  
*foo.email=myemail@mail.com*  
*foo.team=My Sports Team*


______________________

## 9 - SPRING CONFIGURATION WITH JAVA ANNOTATIONS - BEAN SCOPES AND LIFECYCLE METHODS


### @Scope Annotation - Overview

Same as for XML configuration, default scope is Singleton

We can specify a different scope with the @Scope annotation (for the bean)

```java
@Component
@Scope("prototype")
public class TennisCoach implements Coach {
    ...
}
```


### Bean Lifecycle with Annotations - Overview

We can add some custom code during bean intitliazation
For that we use annotations @PostConstruct and @PreDestroy

Process
1. define methods for init and destroy
2. add annotations @PostConstruct and @PreDestroy to the methods

Same remarks as for XML configuration:
* methods can have any access modifier (public, private, protected)
* methods can have any return type. However, we cannot capture any return value, so typically use "void" anyway
* methods cannot accept any arguments
* for prototype beans, the destroy method does not work (Spring does not manage the complete lifecycle of a prototype bean)



__________________

## 10 - SPRING CONFIGURATION WITH JAVA CODE


### Spring Configuration with Java code - Overview

In this case we don't need an XML at all

Reminder 3 ways of configuring the Spring container:
1. Full XML config
2. Annotations (XML component-scan)
3. Java source code

Process
1. create a Java class and annotate it as @Configuration
2. add component scanning support for a package with @ComponentScan (optional)
3. read Spring Java configuration class (AnnotationConfigApplicationContext)
4. retrieve bean from Spring container (getBean())

There are 2 ways to create beans:
1. with @ComponentScan
2. with manual bean creation @Bean (see next paragraph)


### Defining Spring beans with Java code - Overview

Process
1. define method to expose the bean (the name of the method will be the bean Id) in the Config class
2. inject bean dependencies (other @Bean's)
3. read Spring Java configuration class
4. retrieve bean from Spring container


### Injecting values from a Properties file - Overview

Process
1. create Properties file
2. load Properties file in Spring config with @PropertySource("classpath:filename")
3. reference values from Properties file with @Value("${varName}")



__________________

## 11 - SPRING MVC - BUILDING SPRING WEB APPS

https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html


### Spring MVC Overview

Framework for building web applications in Java, based on the MVC design pattern  
It leverages features of the Spring Framework Core (IoC)

Benefits:
* Spring way of building web apps UI
* leverage a set of reusable UI components
* help manage application state for web requests (sessions, etc.)
* process form data (validation, conversion, etc.)
* flexible configuration for the view layer


### Spring MVC - Behind the Scenes

When we receive an incoming request from the browser, it encounters the Spring MVC Front Controller (DispatcherServlet).  
This FC transfers the request to the Controller programmed by us, which contains our business logic.

The Controller manipulates the data through Models and sends it back to the FC, which will turn it into the View template (HTML, JSP...).

Components of a Spring MVC app:
* A set of webpages to layout UI components
* A collection of Spring beans (controllers, services...)
* Spring Configuration (XML files, Annotations or Java)

Interaction with the client's browser is done through the DispatcherServlet, which is provided by Spring. What we have to develop is the MVC:
* Model objects
    * contains the data
	* mapping towards a backend system (database, web service, etc.)
	* can be an object, bean, collection...
* View templates 
	* displays UI layout in the browser (typically html, jsp, jstl)
	* may include data passed from the model
	* very flexible: can be of many types, use templating systems (velocity, thymeleaf, etc.)
* Controller classes
	* contain the business logic
	* handles requests
	* manages the data from/to the model
	* sends to appropiate view template


### Spring MVC Configuration

1. Create a new Web Project (Java EE)
    1. add Spring jars
2. Add configurations to file WEB-INF/web.xml
    1. configure Spring MVC Dispatcher Servlet
    2. set up URL mappings to Spring MVC Dispatcher Servlet
3. Add configurations to file WEB-INF/spring-mvc-demo-servlet.xml
    1. add support for Spring component scanning
    2. add support for conversion, formatting and validation
    3. configure Spring MVC view resolver


in `web.xml`:

```xml
<!-- Spring MVC Configs -->

<!-- Step 1: Configure Spring MVC Dispatcher Servlet -->
<servlet>
<servlet-name>dispatcher</servlet-name>
<servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
<init-param>
<!-- application context configuration file -->
<param-name>contextConfigLocation</param-name>
<param-value>/WEB-INF/spring-mvc-demo-servlet.xml</param-value>
</init-param>
<load-on-startup>1</load-on-startup>
</servlet>

<!-- Step 2: Set up URL mapping for Spring MVC Dispatcher Servlet -->
<servlet-mapping>
<servlet-name>dispatcher</servlet-name>
<url-pattern>/</url-pattern>
</servlet-mapping>
```

in `spring-mvc-demo-servlet.xml`:

```xml
<!-- Step 3: Add support for component scanning -->
<context:component-scan base-package="com.luv2code.springdemo" />

<!-- Step 4: Add support for conversion, formatting and validation support -->
<mvc:annotation-driven/>

<!-- Step 5: Define Spring MVC view resolver. This tells Spring where to look for the template files, and how they are named -->
<bean
class="org.springframework.web.servlet.view.InternalResourceViewResolver">
<property name="prefix" value="/WEB-INF/view/" />
<property name="suffix" value=".jsp" />
</bean>
```

Plus:
1. Add necessary JAR files
    1. javax.servlet.jsp.jstl-1.2.1.jar
    2. javax.servlet.jsp.jstl-api-1.2.1.jar
2. Create folder WEB-INF/view/


__________________

## 12 - SPRING MVC - CREATING CONTROLLERS AND VIEWS

### Creating a Spring Home Controller and View - Overview

First example: homepage

Development process:
1. create controller class
2. define controller method (the name can be anything we want, it's not used, only the @RequestMapping is used)
3. add request mapping to controller method
4. return view name
5. develop view page


### Write some code

1. create a new package


### Reading HTML Form Data

Process
1. Create controller class
2. Show HTML form
    1. create controller method to show the HTML form
        1. add RequestMapping
    	2. return view name
    2. create view page for HTML form
3. Process HTML form
4. create controller method to process the HTML form
    1. add RequestMapping
    2. return view name
5. create view page for Form confirmation


### Adding Data to the Spring Model

* The Model is a container for our application data
* In the Controller we can put anything in the model: Strings, Objects, database info, etc.
* Our View pages (JSP) can access data from the model

```java
// new controller method to read form data and add data to the model
@RequestMapping("/processFormVersionTwo")
public String letsShoutDude(HttpServletRequest request, Model model) {

	// read the request parameter from the HTML form
	String theName = request.getParameter("studentName");

	// convert the data to all caps
	theName = theName.toUpperCase();

	// create the message
	String result = "Yo! " + theName;

	// add message to the model. "message" is the identifier used in the Jsp view through ${message}
	model.addAttribute("message", result);

	return "helloworld";
}
```

*HttpServletRequest* is used to read form data  
Model is just a container for our data, it comes empty and then we can data to it. Data can be in any form: a string, but also any other Object, List, etc.


### How to use CSS, JavaScript and Images in a Spring MVC Web App - **review**

Any static resource is processed as a URL Mapping in Spring MVC. You can configure references to static resources in the spring-mvc-demo-servlet.xml.

In my example, I'm going to have the following directory structure:

![Spring Folder](img/spring_folder.png)

I chose to put everything in the "resources" directory. But you can use any name for "resources", such as "assets", "foobar" etc. Also, you can give any name that you want for the subdirectories under "resources".

**Step 1:** Add the following entry to your Spring MVC configuration file `spring-mvc-demo-servlet.xml`

You can place this entry anywhere in your Spring MVC config file.

```xml
<mvc:resources mapping="/resources/**" location="/resources/"></mvc:resources>
```

**Step 2:** Now in your view pages, you can access the static files using this syntax:

```xml
<img src="${pageContext.request.contextPath}/resources/images/spring-logo.png">
```

You need to use the JSP expression `${pageContext.request.contextPath}` to access the correct root directory for your web application.

Apply the same technique for reading CSS and JavaScript.

Here's a full example that reads CSS, JavaScript and images.

```html
<!DOCTYPE html> 
<html>

<head>
    <link rel="stylesheet" type="text/css"          
           href="${pageContext.request.contextPath}/resources/css/my-test.css">
    <script src="${pageContext.request.contextPath}/resources/js/simple-test.js"></script>
</head>

<body>
    <h2>Spring MVC Demo - Home Page</h2>
    <a href="hello">Plain Hello World</a>
    <br><br>
    <img src="${pageContext.request.contextPath}/resources/images/spring-logo.png" />
    <br><br>
    <input type="button" onclick="doSomeWork()" value="Click Me"/>
</body>

</html>
```


### Deploying your App to Tomcat as a Web Application Archive (WAR) file

When you deploy your Java web apps, you can make use of a Web Application Archive (WAR) file.

The Web Application Archive (WAR) file is a compressed version of your web application. It uses the zip file format but the file has the .war extension.

If you are using Eclipse, then the best way to visualize it is think of your "WebContent" directory being compressed as a zip file with the .war extension.

This includes all of your web pages, images, css etc. It also includes the WEB-INF directory which includes your classes in WEB-INF/classes and supporting JAR files in WEB-INF/lib.

The WAR file format is part of the Java EE / Servlet specification. As a result, all Java EE servers support this format (ie jboss, weblogic, websphere, glassfish and tomcat).

Below, I provide steps on how to create a WAR file in Eclipse. I also show how to deploy the WAR file on Tomcat.

1. In Eclipse, stop Tomcat
2. Right-click your project and select Export > WAR File
3. In the Destination field, enter: <any-directory>/mycoolapp.war
4. Outside of Eclipse, start Tomcat
- If you are using MS Windows, then you should find it on the Start menu
5. Make sure Tomcat is up and running by visiting: http://localhost:8080
6. Deploy your new WAR file by copying it to <tomcat-install-directory>\webapps
Give it about 10-15 seconds to make the deployment. You'll know the deployment is over because you'll see a new folder created in webapps ... with your WAR file name.
7. Visit your new app. If your war file was: mycoolapp.war then you can access it with:  http://localhost:8080/mycoolapp/



_____________

## 13 - SPRING MVC - REQUEST PARAMS AND REQUEST MAPPINGS


### Binding Request Params

Another way to read form data is by using the annotation @RequestParam

The idea is to automatically get the parameter and bind it to the variable. It's a shortcut for:

```java
@RequestMapping("/processFormVersionTwo")
public String letsShoutDude(HttpServletRequest request, Model model) {
        
    // read the request parameter from the HTML form
    String theName = request.getParameter("studentName");
```        

By doing directly:

```java
@RequestMapping("/processFormVersionThree")
public String letsShoutDude(@RequestPAram("studentName") String theName, Model model) {

/* NOT NECESSARY ANYMORE      
// read the request parameter from the HTML form
String theName = request.getParameter("studentName");
*/      
```


### Controller Level Request Mapping

By adding a @RequestMapping to the Controller, we do all the @RequestMapping of the methods, relative to the controler. It's like subfolders for slugs in the URL:

![@RequestMapping](img/spring1.png)



______________

## 14 - SPRING MVC - FORM TAGS AND DATA BINDING


### Spring MVC Form Tags Overview

Spring Form Tags is a feature of spring that eases development of HTML forms:
* configurable and reusable for a web page
	* they generate HTML code automatically
* can make use of data binding
	* automatically set/retrieve data from Java beans

There are many tags available:

| Form tag | Description |
| --- | --- |
| form:form | main form container |
| form:input | text field |
| form:textarea | multi-line text field |
| form:checkbox | check box |
| form:radiobutton | radio buttons |
| form:select | drop down list |

More info:  
https://docs.spring.io/spring/docs/5.0.2.RELEASE/spring-framework-reference/web.html#mvc-view-jsp-tags

we can easily mix the form tags with regular HTML. We only need to add this directive on top of our jsp page:  
`<%@ taglib prefix="form" uri="http://www.springframework.org/tags/form" %>`


This is the big picture:

![FormOverview](img/spring2.png)

1. create Student class with setters/getters for all the properties (First Name, Last Name, etc.)
2. create a StudentController class with 2 methods
* showForm(Model model)
    * instantiates a student object
    * we add this object as an attribute to the model -> this bean holds the data binding of the form
    * returns the student-form.jsp view

```java
@RequestMapping("/showForm")
public String showForm(Model theModel) {
    theModel.addAttribute("student", new Student());
    return "student-form";
}
```

* processForm(@ModelAttribute("student") Student theStudent)
    * we cann pass an annotated argument to make use of the model attribute just created 
    * the object is then populated with the data entered in the form
    * returns a student-confirmation.jsp page where we can print the data properties from the bean

![FormOverview](img/spring3.png)


3. create student-form.jsp view
* this form contains the Spring Form tags
* we create a form aontainer with a modelAttribute, which is the bean instantiated and passed to the model


![FormOverview](img/spring4.png)


* each tag has a path that corresponds to a propery of the bean (theStudent)
	* when the form is loaded, spring calls getter methods to prepopulate the form (placeholder). If properties have null values, form fields will be empty
	* when we click submit, spring calls setter methods the object properties are passed to the model so it can be retrieved 

4. create student-confirmation.jsp
* just to display the data


![FormOverview](img/spring5.png)


Development process
1. Create Student class
    1. create properties and getters/setters
2. Create Student Controller class and form creation code
3. Create HTML Form
    1. add form tags
4. Create form processing code in the Student Controller class
5. Create HTML confirmation page
    1. add display for data binding



### Text Fields

`<form:input path="firstName"/>`


### Drop-down Lists

This is the actual HTML:

```html
<select id="country" name="country"> 
     <option value="Brazil">Brazil</option> 
     <option value="France">France</option> 
     <option value="Germany">Germany</option> 
     <option value="India">India</option>
</select>
```

**Option 1: hardcode options in the JSP file**

Add this to the JSP file

```html
<form:select path="country">
    <form:option value="Brazil" label="Brazil" />
    <form:option value="France" label="France" />
    <form:option value="Germany" label="Germany" />
    <form:option value="India" label="India" />
</form:select>
```

**Option 2: hardcode options in the Student class**

1. define country options in the Student class
    1. declare a private LinkedHashMap
    2. populate it in the class constructor
    3. create getter for the Map
2. add this to the JSP file

```html
<form:select path="country">
    <form:options items="${student.countryOptions}" />
</form:select>
```

**Option 3: Import options from properties file**

https://www.udemy.com/spring-hibernate-tutorial/learn/v4/t/lecture/5940154?start=1


**Option 4: Get options from database dynamically**

see later with Hibernate


### Radio Buttons

Actual HTML

```html
Java <input id="favoriteLanguage1" name="favoriteLanguage" type="radio" value="Java"/>
C# <input id="favoriteLanguage2" name="favoriteLanguage" type="radio" value="C#"/>
PHP <input id="favoriteLanguage3" name="favoriteLanguage" type="radio" value="PHP"/>
Python <input id="favoriteLanguage4" name="favoriteLanguage" type="radio" value="Python"/>
Ruby <input id="favoriteLanguage5" name="favoriteLanguage" type="radio" value="Ruby"/>
```

**Option 1: hardcode options in the JSP file**

Add this to the JSP file

```html
Java <form:radiobutton path="favoriteLanguage" value="Java" />
C# <form:radiobutton path="favoriteLanguage" value="C#" />
PHP <form:radiobutton path="favoriteLanguage" value="PHP" />
Python <form:radiobutton path="favoriteLanguage" value="Python" />
Ruby <form:radiobutton path="favoriteLanguage" value="Ruby" />
```

**Option 2: hardcode options in the Student class**

https://www.udemy.com/spring-hibernate-tutorial/learn/v4/t/lecture/5820486?start=0



### Checkboxes

Similar to Radiobuttons. The difference is that the property in the bean must accept several values --> wen need an ARRAY

* in the form creation add

```html
Linux <form:checkbox path="operatingSystems" value="Linux" />
MacOS <form:checkbox path="operatingSystems" value="MacOS" />
Windows <form:checkbox path="operatingSystems" value="Windows" />
```

* in the Student class, declare operatginSystems as a String[]
* in the confirmation form, loop over every possible value:
    * add the tag: <%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c" %> to provide loop support
	* add the loop

```html
<ul>
    <c:forEach var="temp" items="${student.operatingSystems}" />
        <li>${temp}</li>
    </c:forEach>
</ul>
```


_____________

## 15 - SPRING MVC FORM VALIDATION - APPLYING BUILT-IN VALIDATION RULES


### Spring MVC Form Validation - Overview

Check user input from for:
* required fields
* valid numbers in a range
* valid format (date, postal code...)
* custom rules
* etc.

Java has a standard API, availabel for server-side or client-side apps (JavaFX, Swing)
Spring supports this API, but needs an implementation (eg Hibernate Validator)

What we'll see:
1. set up dev environment
2. validate required fields
3. validate number ranges
4. validate using regular expression
5. create custom validation rules


### Setting up Dev Environment for Form Validation

We will use Hibernate Validator (there are other options)  
http://hibernate.org/validator/


1. Download JAR files from Hibernate website
2. Add JAR files to the project

![Hibernate files](img/spring6.png)



### Checking for required fields

Objective:

![ValidationForm](img/spring7.png)

In this example, only add validation rule to LastName

Process:
1. add validation rule to Customer class
2. display error messages in HTML form
3. perform validation in the Controller class
    1. if the validation is not met, it returns to the form
    2. if it's OK, it goes to confirmation page
4. update confirmation page


Step 1:

![Validation1](img/spring8.png)

> use @NotBlank instead of @NotNull


Step 2:

![Validation2](img/spring9.png)



Step 3:

![Validation3](img/spring10.png)


This is hte important stuff. We add 2 things:

* @Valid says that the model attribute has to be validated
* BindingResult is a container with the results of the validation test


> **Important**: In the method signature, the BindingResult parameter must immediately after the model attribute.that is being bound


Step 4:

update the confirmation page:  
`The student is confirmed: ${student.firstName} ${student.lastName}`

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjk5NDYzNTY4XX0=
-->
