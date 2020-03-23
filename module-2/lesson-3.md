# Lesson 3 - Working with Child Themes

## Changing Styles
The easiest way to update the site is to use CSS in your child theme to override the styles applied to your website. You can use CSS just as you would normally to override and create new styles for your site.

Let’s say we wanted to remove the underline from the buttons on our site. First we need to find out what selector is styling the button. We can look in our developer tools for that.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_1.jpg" alt="" style="max-width:1140px">

In this case it’s
```
.hentry .entry-content a:not(.button):not(.components-button) {
    text-decoration: underline;
}
```
Now we can go to the stylesheet in our child theme and override this style.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_2.jpg" alt="" style="max-width:1140px">

Once added, you will see that the underline from the button has gone as the style for the child theme overrides the parent’s styles.

You can do this with any styles on your site. Find out what selector is styling the element, and override it using your child theme’s stylesheet.

Sometimes it can take a while of searching through the HTML and CSS to find how certain elements are being styled. It’s a good idea to use your developer tools to test and find the styling you’d like to adjust.

Your child theme stylesheet is not just for overriding styles, but can also be used to create new styles.

## Functions.php

The functions.php file is used to add unique features to your theme. It works quite similarly to how plugins add functionality to your website.

You can use functions written by WordPress or you can write your own function. If you look in the parent theme for your site you’ll find a stack of PHP functions which are defining functionalities for the site, and setting which CSS and JavaScript files to use.

In our child theme we can add functions which are new or override functions set in the parent functions.php file.

## Pluggable Functions
A good theme will have a range of pluggable functions which it is possible to plug into your child theme and edit.

The way to spot a pluggable function is an ‘if’ statement which tests whether the function has already been defined in the child theme. If it has already been defined then the parent theme function doesn’t run that function.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_3.jpg" alt="" style="max-width:1140px">

Let’s say we want to update the heading to include our tagline underneath our logo. The first thing we should do is find out what element is containing our logo, and to do that we can inspect the element. It’s a div with class ‘site-branding’.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_4.jpg" alt="" style="max-width:1140px">

Next we can search through our WordPress files for a mention of `<div class="site-branding">`.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_5.jpg" alt="" style="max-width:1140px">

Once you’ve found the PHP file which controls what gets displayed in that section, go to the file which for our theme is called storefront-template-functions.php. Now we could edit it directly in the parent theme, but then we’d never be able to update the parent theme otherwise we’d lose our changes.

Instead we want the changes stored in our child theme. Now because the function is a pluggable function, we can add our changes into our functions.php file.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_6.jpg" alt="" style="max-width:1140px">

Copy everything between line 186 and line 198, leaving the ‘if’ statement behind. Go to your functions.php file in your child theme and type <?php at the very top of the document with no space. Then press enter/return twice and add ?>. In between these lines paste the code you copied from storefront-template-functions.php. Your file should look like this:

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_7.jpg" alt="" style="max-width:1140px">

Now we can just write HTML into the div like so:

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_8.jpg" alt="" style="max-width:1140px">

This is okay, but what if the client wants to change their tagline at a later date, ideally they want to be able to go into Appearance > Customize > Site Info and update the tagline there. To do that we can look in the ‘storefront-template-functions.php’ page and see how the description could be added. The answer is on line 218.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_9.jpg" alt="" style="max-width:1140px">

Copy this if statement and paste it between the PHP tags on line 11 of your functions.php page. And add ‘echo $html’ to add the $html variable to the page. Your functions.php file should then look like this:

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_10.jpg" alt="" style="max-width:1140px">

A simpler version instead of creating the $html variable, is simply to echo the paragraph directly like so:

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_11.jpg" alt="" style="max-width:1140px">

## Editing Template Files

Another way of editing your website using a child theme is to edit the template files.

Let’s say we wanted to add a generic image below each product. First we’d find out which template is editing our product pages. In this case we’re looking for `<div class="summary entry-summary">`.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_12.jpg" alt="" style="max-width:1140px">

Search for that div in your Wordpress files and you’ll find it’s in content-single-product.php which is in WooCommerce’s template files.

Here is where the product details get added to `<div class="summary entry-summary">`.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_13.jpg" alt="" style="max-width:1140px">

Because WooCommerce’s template files are already in your child theme, you don’t need to copy them across. If we were editing a parent theme’s templates, then we would need to copy it across to our own child theme (and create the same folder structure for the file).

I don’t want to edit what gets output in the PHP, I just want to add an image after the div has closed. To do that, I simply add the image into the page (note, I’ve already added the image to my media folder).

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-3_14.jpg" alt="" style="max-width:1140px">

Now on all of the product pages, I will see an image has been added underneath the product info.

## Activities
Activity 2.3.1
For more on working with child themes, please watch the following LinkedIn Learning video (2 hours) https://www.linkedin.com/learning/wordpress-building-child-themes-3/level-up-to-wordpress-developer?u=43268076
3.	Child Themes and CSS
4.	Working with Function Files
5.	Working with Template Files
6.	Add New Functionality

---
- [Go to lesson 4](4)
---
