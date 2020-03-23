# Lesson 1 - Intro to PHP

## Introduction

WordPress is written with PHP and so it’s worth at least knowing the basics of PHP to work with WordPress files.
The first thing to note about PHP is that it’s a server-side scripting language, so it needs to run on a server which is why we have Xampp (or another local server) running when developing locally.
PHP is written in .php files which the server reads and converts to HTML that gets displayed in the browser.


## Getting Started

To start working with PHP, we need to create a .php file. This .php file needs to be on a server. You can place it into your ‘htdocs’ just like your WordPress installation.

To write PHP in our .php file, we need to write our PHP in between tags that start <?php and end ?>

A common statement you’ll see in PHP is ‘echo’ which outputs a string (often HTML) to a page.

```
<!DOCTYPE html>
<html>
  <body>
    <?php
    echo "<h1>Hello World!</h1>";
    ?>
    </body>
</html>
```

In the example above, you will see that a PHP file looks a lot like an HTML file, the only difference is that it uses the PHP tags to add PHP to the page. Here we are adding an h1 to the page saying “Hello world!”. Copy this code and run it in a .php file on your local server. You can place it in a folder in your htdocs folder and then visit the page in your browser, e.g. http://localhost/phptest/index.php

## Variables

A variable name in PHP must start with the $ symbol followed by the name of the variable, and then an equals symbol to set the value of the variable, and then close the line with a semi-colon. Semi-colons are not optional in PHP.

```
<?php
$name = "John Doe";
$age = 35;
?>
```

As you can see, we use quotation marks to create a string, while number variables don’t need quotation marks.

Adding this code to the page will only create the variables. If we wanted to show these variables on the page, we would use the echo statement like so:

```
<?php
$name = "John Doe";
$age = 35;
echo $name;
echo $age;
?>
```
## Concatenation

If we wanted to combine variables and HTML together, we can use concatenation. To do this we use the dot operator (.). The dots act like plus signs in JavaScript.

Let’s say we wanted to add to the page a line that says “John Doe is 35 years old”. We could write the following

```
<?php
$name = "John Doe";
$age = 35;
echo "<p>" . $name . " is " . $age . " years old</p>";
?>
```

See how we use `.` to concatenate variables, as well as how we can write HTML directly into the echo to build the HTML page.

## Learning More About PHP

There is plenty to learn about PHP, but for now these are the absolute basics and will help you understand a bit better what is happening in WordPress’s PHP files.

If you would like to learn more about PHP, you can watch the following LinkedIn Learning video [https://www.linkedin.com/learning/php-essential-training-2/introduction?u=43268076](https://www.linkedin.com/learning/php-essential-training-2/introduction?u=43268076)

---
- [Go to lesson 2](2)
---
