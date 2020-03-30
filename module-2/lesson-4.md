# Lesson 4 - WordPress REST API

Working with PHP can be cumbersome and our scope for what we can develop becomes quite limited by the theme we have chosen.

What if we wanted the advantage of the admin panel for creating content, but wanted to be able to fully customise how that content was displayed by writing our own HTML, CSS and JavaScript? For that, we can use the WordPress REST API.

## Access JSON
The WordPress REST API is a CRUD API meaning we can Create, Read, Update and Delete content. We can Read public data for a WordPress website without authentication, and this includes things like posts and pages created for the site.

If we did want to update any of the content on the API outside of the admin panel we would need to use authentication, but we won’t be going into that in this lesson.

To access the API root for your WordPress website, you can simply add `/wp-json` to the end of the URL.

You can try this on your local version of your WordPress site for Flower Power and you are likely to get something that looks like this.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-4_1.jpg" alt="" style="max-width:500px">

> Please note: the image is from Firefox. If using another browser the JSON might be formatted differently


## Routes
‘routes’ are an address we can use to access information from our site. These routes get added after the URL to view wp-json. For example, because our Flower Power website uses WooCommerce, we can add `/wc/store/products` to the end of our URL and we get a list of products on our website.

<img src="https://raw.githubusercontent.com/MJPhillip/noroff-content-management-systems/master/module-2/images/cms_lesson2-4_2.jpg" alt="" style="max-width:500px">

We can then use these routes to get fetch data from the API and build websites with it.
You can find a list of the available routes for your website on your API’s root at /wp-json. Two common routes you might work with are `/wp/v2/posts` to get a list of the last 10 posts, and `/wp/v2/pages` to get an array of pages.

As you can see, working with WordPress’s REST API is quite simple. If you want more information about using WordPress’s REST API, you can watch this video on LinkedIn Learning. https://www.linkedin.com/learning/wordpress-rest-api-2/restful-wordpress-through-an-api?u=43268076

## Strapi.io
If you’re looking for a headless CMS option that isn’t WordPress, one option is https://strapi.io/ which is a Node.js based open-source solution which allows you to create a customisable REST API and control the content from an easy-to-use admin panel.

---
- [Go to the module assignment](ma)
---
