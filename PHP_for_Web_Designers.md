# PHP FOR WEB DESIGNERS

Questions

* Scope of variables? 2 includes in a file, second takes values of first?


Documentation  
Http://www.php.net



_____________________________

## INTRODUCTION TO PHP

### How PHP makes web pages dynamic

When a browser requests a webpage, it sends a request to the server, which returns an HTML document, along with css, images, js files, etc.

If the requested page is a PHP page, the server itself requests it to the PHP engine (interpreter), which processes it and merges with HTML, that is sent back to the browser. The browser never sees the PHP code

This is a fundamental difference with JavaScript. JS is run in the brower, PHP is run in the server

PHP is very powerful at:

* processing forms
* display different content based on logged in user
* querying a database
* seamlessly integrate with HTML


### How to use PHP in a page

The web server (if it has PHP engine installed) can treat the PHP code, but to do that we have to provide a file named *.php

Inside the file, PHP code goes between these:

```php
<?php // PHP code in here ?>
```

Each block is independent, we can't nest PHP blocks inside another

Statements must end with ";"


### Using variables to store information

Variables are declared beginning with $, camelCase name

* digits (not 1st one)
* letters
* _
* case-sensitive
* cannot use $this (reserved keyword)



The ISSET() function checks if the variable exists (boolean)


### Storing numbers and text in variables

```php
$answer = 42;
$price = 10.99;
$title = "The Hitchhiker's Guide to the Galaxy";
$author = 'Douglas Adams';
$description = 'A hilarious romp through space and time,
in which we learn the ultimate answer to life, the
universe, and everything. You will love the book, but
maybe not the answer:';
```

We can split text over several lines



### Displaying the value of number and text variables

Normally in a real website, the values of variables will be obtained from a database

```html
<p>This week's recommended reading:</p>
<h2><?php echo $title; ?></h2>
<p class="author">by <?php print $author; ?></p>
<p><?= "$description $answer"; ?></p>
<p>Price: $<?php echo $price; ?></p>
```
echo and print is basically the same, so use echo  
`<?=` is a shortcut for `<?php echo`  
If we put a string and variables between " ", the variable  is replaced by it's value  
If ' ', the var name will be printed literally



### Using functions to manipulate values

PHP has a huge built-in library

We call a function by his name, and passing the arguments needed:

```php
function(arg1, arg2);
```


### Adding comments to PHP scripts

PHP has 3 types of comments inside PHP code:

```php
// single line comment

# single line comment

/* multi 
    line
    comment */
```


__________________

## USING SERVER-SIDE INCLUDES FOR COMMON PAGE ELEMENTS

### What are server-side includes?

One of the most powerful features of PHP  
Basically it's like external CSS sheets: centralize a piece of PHP code and include it in every page we want

```php
<?php include 'includes/path/to/file' ?>
```

Include files

* are usually stored in a folder /includes
* can have any extension, but most common is .php
* can contain any type of code, php, html, but just the code to be included in other files



### Deciding which include command to use

There are actually 4 types of include directives:

* include -> if can't find the file, script continues execution
* require -> if can't fine the file, script stops execution
* include_once -> aims at avoiding "redefined fatal errors" in complex programming environments
* require_once -> aims at avoiding "redefined fatal errors" in complex programming environments



### Challenge: Moving common elements to include files

He takes the header and navigation menu to one require, and the footer to an include

In the top level files the include path is /includes/, in the subfiles it is ../includes/


### Making sure internal links still work in an include file

In the php file, the path to the include should be relative to the file.  
Inside the include, paths and links should be absolute  
We can use a variable to store the siteroot  

```php
<?php echo $siteroot; ?>
```

____________________

## USING CONDITIONS TO CHANGE PAGE OUTPUT

### How PHP makes decisions

```php
if(condition) {
    // Code
} elseif(condition) {
    // Code
} else {
    // Code
}
```

Comparison operators are the same as in Java

Note: the code between {} doesn't have to be PHP, it can be HTML. In fact, it's more efficient to write plain HTML rather than echoing it from PHP.


### Changing output depending on the current time

We can use the function `date();`

There are many flavors of it, check the docs



### Adjusting the server's time zone

We can do that in PHP.ini  
Check with the hosting provider  

If in Apache, we can also set in .htaccess 

```php
php_value date.timezone 'America/Los_Angeles'
```

Else, we can set it directly in the script with the function
date_default_timezone_set('America/Los_Angeles');


### Displaying an up to date copyright notice

Small snippet in footer.php  
Checks current year vs startYear and displays `$copyright = "$startYear&ndash;$currentYear"`



### Challenge: displaying an image of the month

```html
<?php
$currentMonth = date('M');
$currentMonth = strtolower($currentMonth);
?>

<img src="images/special_<?php echo $currentMonth; ?>.jpg" alt="Fresh Tulips" height="200" width="450"> </a>
```


### Understanding what PHP treats as true and false

These are "faulsy" values in PHP:

* Keywords FALSE and NULL (case insensitive)
* Zero (0, 0.0, '0', '0.0')
* An empty string ('', "")
* An array with 0 elements
* A SimpleXML object created from empty tags


Everything else is true


_________________

## WORKING WITH MULTIPLE VALUES IN ARRAYS AND LOOPS

This chapter sets the ground for working with online forms and retrieving values from a DB: the input from a form is stored as an array, and each row of a DB query is an array too

An array is a variable that stores multiple values. A loop allows to get each individual value in turn.


### Storing multiple values in a variable as an array

There are 2 ways to create an array

First:
```php
$flowers = array('tulips', 'roses', 'orchids');
```

Second (PHP 5.4+):
```php
$flowers = ['tulips', 'roses', 'orchids'];
```

To add a new element (at the end of the array)
```php
$flowers[] = 'irises';
```

> Arrays are zero-indexed


### Inspecting an array's elements

We can use the function

```php
print_r(array);
```

To display the contents of an array in a formatted string. It's not good for a webpage, but good for dev purposes, use `<pre>` tags

To display a specific value:

```php
echo $flowers[3];
```


### Challenge: inserting the appropriate alt text

Create an array of 12 alt texts  
use function `date('n');`


### Displaying an array as a comma-separated list

Unlike JavaScript, PHP doesn't automatically convert an array to a string

We have to do it using a function called implode
Opposite, explode breaks a string into an array

```php
<?php echo implode(separator, array); ?>
```

### Looping through an array's values

Loops allow us to access each element in turn 

There are many types of loops in PHP, here we see only foreach

```php
foreach($myArray as $tempVar) {
    // code on $tempVar;
}
```

There are also the keywords continue and break


### Labeling array's elements

By default, arrays are indexed. Each value is accessed by its index positoin

But we can also create labeled arrays, aka associative arrays (like dictionaries)

To create one:

```php
$seasons = array(
    'winter' => 'This is winter',
    'spring' =>'This is spring', 
    'summer' => 'This is summer',
    'autumn' => 'This is autumn',
);
```

To display a specific element:

```php
<?php echo $seasons['spring']; ?>
```


### Looping through an array's labels and values

Associative arrays can be looped just like indexed arrays

```php
foreach($seasons as $season) {
   echo $season;
}
```

But we can also access keys (labels) as well as values

```php
foreach($seasons as $key => $value) {
   echo "The caption for $key is $value";
}
```

Here we use 2 temporary variables, we can name them as we want



### Finding if a value exists in an array

We could loop through the array to check if a value exists. But it's more efficient to use the `in_array($itemToCheck, $array)` function



### Challenge: Displaying a seasonal feature

We have to display an image and tagline based on the month inwhich we are.

```php
$features = array(
    'winter' => 'RPP: Beautiful arrangements for any occasion.',
    'spring' => 'It must be spring! Delicate daffodils have arrived.',
    'summer' => "It's summer, and we're in the pink!",
    'autumn' => "Summer's over, but our flowers are still a riot of colors."
);

$seasons = array(
    'winter' => array('dec', 'jan', 'feb'),
    'spring' => array('mar', 'apr', 'may'),
    'summer' => array('jun', 'jul', 'aug'),
    'autumn' => array('sep', 'oct', 'nov')
);

$currentSeason = '';
foreach($seasons as $season => $months) {
    if (in_array($monthname, $months)) {
        $currentSeason = $season;
        break;
}
}
```

__________________

## GETTING USER INPUT FROM A FORM

### Getting form input sent by the POST method

HTML provides all the elements needed to build an online form, but it's not capable of processing the data once the form has been submitted. For that, we need a server-side language such as PHP.

With POST method, the data is sent in the HTTP headers to the server.  
If we do not provide an action in the form, the same form page is reloaded

When the server receives a form request, PHP automatically creates an array called "$_POST" that contains any data submitted by the post method. It's an associative array that uses the "name" attributes of the HTML form elements as keys.  
We can use the name of the submit button to test if the form has been submitted:

```php
if( isset($_POST['submit_button'])) {
}
```

### Retrieving values from a URL's query string

There are 2 methods of submitting a form:

* POST, transmits input data in the background with the HTTP headers
* GET, adds input data into the URL, in series of name/value pairs


PHP automatically creates an array called `$_GET` that contains any data submitted by the post method. It's an associative array that uses the "name" attributes of the HTML form elements as keys.


### Challenge: plan the order form

1. Display the contents of the array (print_r)
2. identify a pattern
    * each flower has a color/qty/cost
    * if no color, only image
3. create a different array for each qty, color and cost
    * we look for the substring position in qty, color or cost
    * we extract the remainng substring as key for the new array
    * we assign to the new array['key'] the original value
4. process the data in the new arrays to build a table in oredr.php to display the order contents
5. control the rows:
    * assign the correct image
    * show only flowers with qty > 0
    * if no flowers, display message "bouquet is empty"
6. Display the column "color"
7. Display the price of the bouquet
    * display the cost for each flower
    * display the TOTAL cost of the bouquet
    * display the shipping charges
8. Create session variables so that we do not lose our bouquet if we go to another page



### Finding and extracting a substring

We can use the function `strpos(string, substring))`  
which returns the index position of the beginning substring

Then another function to extract the substring: `strsub(string, position, [length])`

To extract the substring beginning at the given position


### Organizing the form data into arrays

We build an array for color, qty and image, for each key as flower. The prices we set them in a hardcoded array, to prevent spoofing

Logic:

```php
if (isset($_POST['bouquet'])) {
    $color = array();
    $quantity = array();
    $image = array();
    foreach ($_POST AS $key => $value) {
        if (strpos($key, 'color_') === 0) {
            $color[substr($key, 6)] = $value;
        } elseif (strpos($key, 'qty_') === 0) {
            $qty[substr($key, 4)] = $value;
        }
        if (strpos($key, 'image_') === 0) {
            $image[substr($key, 6)] = $value;
        }
    }
}
```

### Using a loop to build a table for the data

We use a different syntax for the foreah loop, instead of curly braces {} we use endforeach keyword
This is just to simplify and not use too many confusing {}

```html
<?php foreach ($quantity AS $flowername => $amount):                    ?>
    <tr>
        <td><img src="images/160_calla_blush_160337318.jpg" alt="" width="80" height="80"/></td>
        <td><?php echo str_replace('_', ' ', $flowername); ?></td>
        <td>&nbsp;</td>
        <td><?php echo $amount; ?></td>
        <td>$</td>
    </tr>
<?php endforeach; ?>
```


### Controlling which rows are displayed

First we need to display the right image

```html
<td><img src="images/<?php
    if (isset($color[$flowername])) {
        echo $color[$flowername];
    } else {
        echo $image[$flowername];
    }
    ?>.jpg" alt="" width="80" height="80"/></td>
```
Then, display only flowers with qty > 0

```php
if ($amount > 0) :
endif;
```

Finally, check if the basket is empty at all:

```html
<?php if (!isset($quantity) || array_sum($quantity) === 0) { ?>
<p>Your basket is empty.</p>
```

`array_sum($array)` sums the numbers in an array


### Creating a custom function to extract part of a file name

To extract the color: we identify the pattern "number_flower_color_id"

we can use the function "explode" to build an array using "_" as separator. Then take the 3rd element of the array as color:

```php
<td>
<?php
if (isset($color[$flowername])) {
    echo getColor($color[$flowername]);
    } else {
        echo '&nbsp;';
    }
?>
</td>
```

We build a custom function to get the color:

```php
function getColor($filename) {
    $parts = explode('_', $filename);
    return ucfirst($parts[2]);
}
```

We do that with the function keyword
ucfirst makes the first letter uppercase


### Calculating the order total

First, we declare a variabel to store the TOTAL
```php
$total = 0;
```

Then for each flower we display its cost, and sum it to the total

```php
<td>$<?php echo $cost = $amount * $price[$flowername];
                        $total += $cost; ?></td>
```

Finally we display shipping and TOTAL

```html
<tr>
    <td colspan="4">Shipping</td>
    <td><?php
            if ($total < 75) {
                echo '$10';
                $total += 10;
            } else {
                echo 'FREE';
            } ?>
    </td>
</tr>
<tr>
    <td colspan="4">Total</td>
    <td>$<?php echo $total; ?></td>
</tr>
```


### Using PHP sessions to preserve data

A common way to store data temporarily is by using cookies  
These are name/value pairs that are stored in the browser, and sent to the web server on each page request. The disadvantage is that the same information s sent round-trip upon every page request, so unnecessary bandwidth consumption

PHP offers an alternative approach using sessions. The difference with cookies is that sessions are stored in the server, rather than the browser. The browser only stores and sends 1 piece of information: a session ID. This ID is sent on each request. If the server is using a session, it will retrieve the data for this ID, build the page based on it, and sent it back to the browser under HTML

This makes it possible to preserve form data until it's needed, or to keep users logged into the site

All we need is a command session_start() as close to the top of the script as possible  
Session variables are created by assigning values to the $_SESSION array, another superglobal array

`$_SESSION` is an associative array, so as to store data we use as key the variable name:

```php
$_SESSION['username'] = 'Ramon';
```

To store an array we chain []. For example an associative array:

```php
$_SESSION['quantity']['daisies'] = 2;
```

These variables will be available on all pages of the site that use the session_start();

In theory, not all the pages need the session_start(), only those where we need to access the session variables


### Storing data in session variables

We need to declare session_start(); in order.php
Plus, replace every instance of our variable arays with the $_SESSION equivalent

For example:

```php
session_start();
if (isset($_POST['bouquet'])) {
    foreach ($_POST AS $key => $value) {
        if (strpos($key, 'color_') === 0) {
            $_SESSION['color'][substr($key, 6)] = $value;
        } elseif (strpos($key, 'qty_') === 0) {
            $_SESSION['quantity'][substr($key, 4)] = $value;
        }
        if (strpos($key, 'image_') === 0) {
            $_SESSION['image'][substr($key, 6)] = $value;
        }
    }
}
```

Also we need to move the $price array out of the if statement, because we may go back to the cart (order.php) without going through the submit form


### Ending the PHP session and deleting the data

We should always delete session variables when no longer needed

We can delete them individually, or we can delete them all at once

We use the unset() function

For example to deltee a single variable:

```php
unset($_SESSION['quantity']['Peruvian Lilies']
```

To delete all variables, we just need to declare it as an empty array:

```php
$_SESSION = array();
```

Finally, to end the session we do:

```php
session_destroy();
```

This clears the session ID


___________________

## DISPLAYING CONTENT FROM A DATABASE

### Loading data into MySQL

The ability to connect to a DB is one of the most compelling reasons to work with PHP

PHP is able to work with a wide range of databases

We will work here with mySQL 

In XAMPP, connect to phpMyAdmin

* create database
* import arrangements.sql
* add user and privileges


### Connecting to the database

PHP provides 3 API to work with MuSQL:

* MySQL
* MySQLi
* MySQL_PDO


Recommended is mysqli

There are 2 ways to connect to MySQLi:

* procedural
* object-oriented


Where we use OO

```php
$message = '';
$db = new MySQLi('localhost', 'username', ''password', 'db_name');
if ($db->connect_error) {
    $message = $db->connect_error;
} else {
    $message = 'Connection is OK';
}
```


### Querying the database

```php
$message = '';
$sql = 'SELECT * FROM table';
$result = $db->query($sql);
if ($db->error) {
    $message = $db->error;
}
```


### Displaying the results of the query

We use the fetch_assoc() function,. which creates an associative array for each row, where the keys are the column names, and the values are the column values

```php
while ($row = $result->fetch_assoc()) {
    echo $row['column_name1'];]
    echo $row['column_name2'];]
    // etc...
}
```

This queries 1 row at a time, which is pretty easy

Let's see in the next chapter how to display several elements per row (for other HTML layouts)


### Using modulo division to establish a repeating series

The modulo operator '%' returns the remainder of a division, but the syntax is different from Java:

```php
0 % 4 = 0
1 % 4 = 1
2 % 4 = 2
3 % 4 = 3
4 % 4 = 0
5 % 4 = 1
```

We can use this technique to display or not the opening and closing HTML tags of our unordered list

This is used to wrap every item_:

```html
 <li> 
    <a href="details.php"> <img src="../images/<?php echo $row['image']; ?>" alt="<?php echo $row['alt']; ?>" height="200" width="200">
    <h3 class="h4"><?php echo $row['title']; ?></h3>
    <p class="reset">From $<?php echo $row['price']; ?></p>
    </a> 
</li>
```

This precedes only the 1st of a 4-in-row

```html
<div class="section">
<ul class="reset tiles">
```

This appends the last of a 4-in-row

```html
</ul>
</div>
```


### Repeating output at specific intervals in a loop

```html
<div class="page open">
<?php
    $i = 0;
    while ($row = $result->fetch_assoc()) {
        if ($i % 4 === 0) { ?>
            <div class="section">
            <ul class="reset tiles">
        <?php } ?>
    <li> 
        <a href="details.php"> <img src="../images/<?php echo $row['image']; ?>" alt="<?php echo $row['alt']; ?>" height="200" width="200">
        <h3 class="h4"><?php echo $row['title']; ?></h3>
        <p class="reset">From $<?php echo $row['price']; ?></p>
        </a>
    </li>
    <?php $i++;
        if ($i % 4 === 0) { ?>
        </ul>
        </div>
        <?php } // end if
    } // end of loop ?>
</div>
```


### Linking to a details page

Here we adapt the code so that we click on an image, we go to the details page of the corresponding image

We do that using the id in the GET query:

```html
<li> <a href="details.php?id=<?php echo $row['id']; ?>">
```


### Embedding a variable in a query securely

This is to prevent SQL injection (does not go into detail)

There are several possible approaches, one of them is to use the "real_escape_string" function

We add this to the top of details.php

```php
<?php
$message = '';
$db = new MySQLi('localhost', 'phpwebdes', 'lynda', 'hanselandpetal');
if ($db->connect_error) {
    $message = $db->connect_error;
} else {
    $sql = 'SELECT * FROM arrangements WHERE id' . $db->real_escape_string( $GET['id'] );
    $result = $db->query($sql);
    if ($db->error) {
        $message = $db->errorM
    } else {
        $row = $result->fetch_assoc();
    }
}
?>
```

Then in the rest of the page we replace HTML page with php echo from the id entry in the database (title, alt, image, price, etc...)



### Handling database errors gracefully and securely

Error messages are necessarily for debugging, but in Production, we should hide them, in order to prevent sensitive information from being exposed

The basic idea is that, wherever we echo something from the database, we first check if there has been an error ($message is TRUE). If not, we output the echo from DB, if yes, we replace with an HTML message like "Oops, there has been an error"

To also hide connection errors to the database, we can add this on top of any page where we connect to the DB:

```php
ini_set('display_errors', '0');
```

If that is not already turned off by our server


______________________

## HANDLING ERRORS

### Dealing with PHP errors

Unlike HTML and CSS errors, where the browser renders the page anyway, errors in PHP will most likely render a blank or errored page

In this page we review some of the most common error messages, which btw, are not very beginner-friendly

Firs thing to do is display phpinfo(); on our server, to see if display_Errors is On/Off.  
It should be On in dev env, but Off in Production  
Errors look ugly and unprofessional. Plus, it can display sensitive information

We can change settings in .htaccess for example  
Also, depending on the hosting, in .user.ini


### Why is my page blank or incomplete?

Blank page is proboably because display_error_messages is OFF.   
In dev environment, we should turn it on

Otherwise, probably there's a syntax error. Check in an IDE


### Tracking down parse errors

These are the most common  
It means the PHP interpreter could not parse the .php file => there is an error in the PHP code syntax  
Normally, the error message tells us the line

A very common error is an "unexpected end of file"  
This means that there is a missing closing something ("?>", "}", ...)  
Typically, it is a missing "}"  

Having an editor is very helpful to spot errors


### What to do with "failed to open stream"?

This is normally due to require/include files not found  
Always use a path relative to the current document  
Also check for file permissions  


### What does "headers already sent" mean? 

It may be associated to a session_start, that cannot be started ibecause the HTTP headers have already been sent  
And they have been sent because there is something already sent through HTTP, probably a space " " or line before the opening <?php at the beginning of the file

Or also maybe blank spaces at the end of an external file included earlier  
A solution for that is to leave out the closing PHP tag in an include file that only contains php code


### What does "undefined index, variable or constant" mean?

"Undefined variable" specifies that we are trying to use a variable that has not been declared
-> Probably typo

"undefined index" is related to an associative array, not founding the key variable

"undefined constant" is like variable for a constant, for example in `$array[key]` instead of `$array['key']`

Another problem typically occurs when the error is produced sometimes yes, asometimes not. And this is probably because a variable defined inside an IF statement


### What is T_ENCAPSED_AND_WHITESPACE?

This is because we have put an associative array inside " "

This is not allowed:

```php
<?php echo "The slogan is $slogan['mySlogan']"; ?>
```

We have to wrap it into {}

```php
<?php echo "The slogan is {$slogan['mySlogan']}"; ?>
```
