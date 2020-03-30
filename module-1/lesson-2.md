# Lesson 2 - How to get set up with WordPress

WordPress uses PHP, a server-side language, to render pages; therefore we need to run WordPress on a server. When developing, it’s best to install WordPress on your local machine so that you can make changes in case something breaks. When you’re finished developing, you can upload your WordPress site to your web host.

## Getting an Interview

### Step 1 – Local server

Download an application to run a local server on your computer.

There are a few to choose from, but Xampp, Wamp or Mamp are some of the most commonly used. Xampp can run on Windows, Mac or Linux. Wamp runs on Windows and Mamp runs on Mac.

In our example we’re going to be running Xampp which you can download from [https://www.apachefriends.org/index.html](https://www.apachefriends.org/index.html).

Once downloaded and installed you should be able to open an application that looks like this:

<img src="/images/cms_lesson1-2_1.jpg" alt="Xampp Control Panel" style="max-width:600px">

> Please note:
Mac users might prefer to choose [MAMP](https://www.mamp.info/en/windows/) from the beginning as it is well suited for Mac users.

Click ‘Start’ for both Apache and MySQL and you can test that your server is running by going to http://localhost/ in your browser which should load up a page saying ‘Welcome to Xampp.

### Step 2 – Download WordPress files

Next you need to download the WordPress files from [https://wordpress.org/download/](https://wordpress.org/download/). Take the zip file you’ve downloaded and copy it.

Navigate in your file explorer to where you have installed Xampp. On a Windows PC it will most likely be C:\xampp. For Mac go to the Volumes tab, click Mount and then Explore.

<img src="/images/cms_lesson1-2_2.jpg" alt="Xampp htdocs" style="max-width:600px">

Now click into the htdocs folder and create a new folder called ‘flower-power’. Inside this folder paste your zip file with all your WordPress files and extract.

<img src="/images/cms_lesson1-2_3.jpg" alt="WordPress files in htdocs" style="max-width:600px">

### Step 3 – Create a Database for WordPress

It’s important to understand the relationship WordPress has with its database. All of the posts, pages and comments that are made on WordPress’s admin side are stored in this database. To create a MySQL database go to http://localhost/phpmyadmin/ and click Databases

<img src="/images/cms_lesson1-2_4.jpg" alt="phpMyAdmin" style="max-width:600px">

Enter a database name called ‘flower-power’ and click create.

### Step 4 – Run the WordPress install

Go to localhost/flower-power which will begin the installation wizard. First you’ll be asked for a language for the install, next an overview of what is needed where you can click “Let’s go”.

Enter ‘flower-power’ as the database name. Set the username to “root”, leave the password blank and leave database host as localhost and table prefix as wp\_.

<img src="/images/cms_lesson1-2_5.jpg" alt="WordPress install" style="max-width:600px">

It is important to note that this only works for an installation on your local computer. When you upload the website to your web host you’ll need to create a user and assign them a password with access to the database.

Next click ‘Run the installation’. Now set the Site Title to ‘Flower Power’, create your username and password which you must store somewhere as it will be needed. Add your email address and discourage search engines from indexing the site.

Finally click Log in and input your username and password you just created. You should now be logged into your WordPress admin site.

<img src="/images/cms_lesson1-2_6.jpg" alt="WordPress dashboard" style="max-width:600px">

If you would like to follow an installation video for WAMP or MAMP you can watch the following videos. [WAMP](https://www.linkedin.com/learning/installing-and-running-wordpress-wamp-2/welcome?u=43268076) and [MAMP](https://www.linkedin.com/learning/installing-and-running-wordpress-mamp-2)

---

-   [Go to lesson 3](3)

---
