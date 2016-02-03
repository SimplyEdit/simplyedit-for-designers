#First steps

The first thing you need is a website. Just the HTML will do. But you will have to host it on a webserver somewhere. If you try to use SimplyEdit on a HTML file somewhere on your disk directly, none of the javascript code will run. Since SimplyEdit is all about javascript, that won't work.

You can use any kind of webserver. You can even use github to host your website. Github is a website used mostly by programmers to store and share their sourcecode. But you can also use to create and host a website. There's an entire chapter about Github later on. 

If you have no webserver or host yet, you could take a look at the list at http://b2evolution.net/web-hosting/budget-web-hosting-low-cost-lamp.php for some cheap options. These sites all make it very easy to get started. 

To make the rest of the examples in this book, just make sure that you do select support for  PHP 5.4 or higher. You don't need a database or a CMS to use SimplyEdit. There is also no requirement to use PHP, but it is one of the simplest ways to get everything to work. If you want to know about alternatives to PHP, take a look at the SimplyEdit for Developers book.

##Create your homepage

If you have the hosting sorted, the next step is to create a homepage for your website. You can just create a complete site from scratch with just plain HTML and CSS, but its a lot quicker if you download one of the example websites from https://simplyedit.io/examples/.

Just unzip the contents directly in to your website root directory. You'll see something like the following list of files:

- `index.html`
- `style.css`
- simply-store/
  - `.htaccess` 
  - `put.php`
  - `router.php`
  - data/
    - `data.json`
  - images/

First open the site in your webbrowser. It is just a standard website. Now click on the 'Edit me' button that should be in the top right corner. Now you can edit your website.

However, you can't save your changes yet. For that you need to do a few more things:

1. Get a trial key from https://simplyedit.io/. You can get one for free, it will work for 30 days. You can only get a trial key once for each seperate domain though.

2. Edit the `index.html` file and, in the script tag at the bottom, replace the string `simplyedit-demo-key` with your new trial key.

3. Make sure that the directories `data/` and `images/` can be written to by the webserver. How to do this depends on where you host your site. Usually you can change the 'owner' of the file to a specific username like `www-data`. Under no circumstance must you make these directories writable by everyone. That is just asking for trouble.
 



