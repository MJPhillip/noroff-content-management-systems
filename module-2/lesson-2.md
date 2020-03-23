# Lesson 2 - Child Themes

Themes are great for getting a site set up with a layout that works, but what happens if you would like to change a few aspects of the look and feel while keeping the same theme?

Child themes are used to modify a theme installed on your site. You keep the original theme as a parent theme, but can then target specific elements and files to update and change in the child theme.

When your website gets loaded, styles in the child theme will be loaded last, and as we can remember from CSS, the last style declared is the style which gets applied. If you don’t change the style in the child theme, the original styling from the parent theme will be applied.

For template files in the child theme, they will be loaded first and only if they aren’t loaded by the child theme, will the parent theme templates get loaded.

WordPress and its themes are regularly being updated and so using child themes is a way to ensure styling we have added remains the same, even if the parent theme gets updated. That way you get the latest features for your theme, without breaking the unique changes you’ve made.

It’s a good idea to be careful about choosing a parent theme for your site as the more you have to modify in the child theme, the more work you’re going to have.

## Setting up Child Theme

Open your WordPress files in your text editor. Go to wp-content > themes and create a folder called ‘flower-power’. It is also a common standard to name the folder your theme name plus ‘-child’, so storefront-child is another valid folder name.

Inside that folder create a style.css file and a blank functions.php file.

Next we have to add very specific information to the style.css file. Copy the following and add it directly to your stylesheet.

```
/*
 Theme Name:   Flower Power
 Theme URI:
 Description:  Storefront Child Theme
 Author:       YOUR NAME HERE
 Author URI:
 Template:     storefront
 Version:      1.0.0
 License:      GNU General Public License v2 or later
 License URI:  http://www.gnu.org/licenses/gpl-2.0.html
 Tags:         light, dark, two-columns, right-sidebar, responsive-layout, accessibility-ready
 Text Domain:  storefrontchild
*/
```

Now you should be able to go to the admin page for your site and go to Appearance > Themes and you will see your theme is coming through. Click activate on your child theme.

Storefront makes creating child themes easier than some other themes, and so we don’t need to enqueue any of the parent theme style files with PHP from the theme’s functions.php file or @import these into the child themes style.css.

You can now try write a style in your styles.css file to see it coming through. Maybe update the body color or choose another element to style and make sure everything comes through correctly.
For a tutorial by WordPress on adding a child theme, please go to [https://developer.wordpress.org/themes/advanced-topics/child-themes/](https://developer.wordpress.org/themes/advanced-topics/child-themes/)

If you’d like to follow along with a tutorial to set up a child theme you can watch Wordpress: Building Child Themes [https://www.linkedin.com/learning/wordpress-building-child-themes-3/level-up-to-wordpress-developer?u=43268076](https://www.linkedin.com/learning/wordpress-building-child-themes-3/level-up-to-wordpress-developer?u=43268076)
1.	Building on a Solid Foundation
2.	Creating a Child Theme

---
- [Go to lesson 3](3)
---
