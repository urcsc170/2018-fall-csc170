# Lab 15: Menu Highlighter Plugin
*Due: Thursday, November 29, 2018*

In a previous lab, you factored-out your NAV element from your HTML documents and put it in a PHP Include file which broke the "is-current" feature.  In this lab, you will use a solution to programmatically put it back using a jQuery-powered Plugin.

## Step 1: Install the Menu Highlighter Plugin

- [ ] Make a copy of your **lab14** folder.  Call it **lab15**
- [ ] [Download the **menu-highlighter.js** file (in a ZIP file)](menu-highlighter.zip), extract the JS file and put it in the **js** folder in your **lab15** folder

Note:  The **menu-highlighter.js** file will automatically insert the "is-current" class on the appropriate menu item in the navigation.  But you have to install the **menu-highlighter.js** file on every page to make it work.  But instead of doing that on every page…

## Step 2: Create a scripts.inc file

- [ ] Create a new *include* file in the **inc** folder named **scripts.inc**  

- [ ] In the **scripts.inc** file, install jQuery (because the menu highlighter plugin uses jQuery) and then install the plugin like this:

	```html
	<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.0/jquery.min.js"></script>
	<script src="js/menu-highlighter.js"></script>
	```


- [ ] Then in the appropriate place on each webpage (above the closing BODY tag) use the PHP code to include the scripts.inc file like this:

	```php+HTML
	<?php include "inc/scripts.inc"; ?>
	```

  - Note that the **index** page, the jQuery installation already exists.  You must never install the same library twice on the same page!  So…

- [ ] In the **index** file, REMOVE the SCRIPT tag that installs jQuery.  And then insert the PHP include that points to the **scripts.inc** file in its place, *above* the other JS `<script>` tags for **SSS** and **jQuery UI**

## Part 3: Upload your Work

When you are done with your webpage, close everything and use an FTP tool to access your account on **csc170.org** and upload your files:

- [ ] In a web browser (any), go to this address to check your handiwork: 
		`www.csc170.org/accountname/lab15`
	(where “*accountname*” is your account name)

When you look at your Lab 15 website in your browser as it's being served from the class web server:

- [ ] All the Include statements should work on each webpage -- each page should look normal (as if the PHP includes didn't exist)
- [ ] The current menu highlighter should work
- [ ] The plugins on the homepage (SSS, and the jQuery UI accordion)

…if not, you have some debugging to do.  Good luck!  Figure it out.

## Part 4:  Report your work

In our Blackboard section, in Lab 15, post a link to your website to receive credit for this Lab.