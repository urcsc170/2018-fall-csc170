# Lab 10: PHP Includes
*Due: Thursday, October 25, 2018 (one week)*

For this lab, you will take your existing website from your lab assignments and factor out some of the duplicate code, and place the duplicate code in *Server-Side Includes* using PHP.

## Part 1: Setup

- Make a copy of your lab09 folder and name the new folder **lab10**

## Part 2: Change the files from HTML to PHP

- Change the file extensions of all the HTML files from **.html** to **.php**
  - Change the file extension of your *start.html* file too

Reminder: after you change the file extensions you can no longer view your web pages by simply double-clicking on the HTML files. From here on out, you're working "blind" until you upload your files to the web server. 

*The exception to this is: if you load a "WAMP" stack or "MAMP" stack on your computer.  That would allow you to view PHP files on your own computer, but that's not necessary for CSC 170.  If however, you're interested in doing that anyway, use the instructions demo'd in the lecture.*

## Part 3: Setup the new "include" files

- Inside the **lab10** folder create a new folder named **inc**
- In the **inc** folder create two new plain text files with these names:<br>**html-top.inc**<br>**nav.inc**
- Open all the **.php** files (the files that used to be .html) in your code editor
- Open both **.inc** files in your code editor

The rest of this lab requires you to juggle a lot of open files while copying and pasting code between them. It's easy to make mistakes and mess thing up. Go slowly!

## Part 4: Replace the header HTML with a PHP Include script

- Pick any one of your **.php** files EXCEPT the **start.php** file.  *Copy* the following code to your computer's clipboard...

```html
<!doctype html>
<html lang="en">
<head>
	<meta charset="utf-8">
	<title>Lab 8 – Shakespeare</title>
	<link rel="stylesheet" href="css/styles.css">  
	<link rel="stylesheet" href="css/navigation.css">
</head>
```

...and paste it into the file: **html-top.inc**

*(Don't use your start.php file because it doesn't have the link to the "navigation.css" file!)*

- [ ] Edit the code in the **html-top.inc** file – update the lab number: "**Lab 8 - ...**" to "**Lab 10 - ...**"
- [ ] In ALL five PHP files (that's the webpages, including start.php) replace the top part (the doctype down to the closing HEAD tag) and insert a PHP Include statement that points to the **html-top.inc** file 

## Part 5: Replace the menu HTML with a PHP "include" script

Note: doing this step will break the "is-current" menu highlighter. That's okay. We'll fix it in a later lab assignment.

- In any of your **.php** files except the **start.php** file, *copy* the following code to your computer's clipboard...

```html
<nav class="menu">
	<ul>
		<li><a class="is-current" href="cats.html">Cats</a></li>
		<li><a href="dogs.html">Dogs</a></li>
		<li><a href="fish.html">Fish</a></li>
		<li><a href="bears.html">Bears</a></li>
	</ul>
</nav>
```

...and paste it into the file: **nav.inc**

*(Don't use your start.php file because it doesn't have a NAV element!)*

- Edit the code in the **nav.inc** file: 
  - Replace every instance of **.html** with **.php**
  - Remove the `class="is-current"`
- In ALL five PHP files replace the entire NAV element with a PHP Include statement that points to the **nav.inc** file 
  - Although the *start.html* file didn't have a NAV element, go ahead and add the PHP Include for the nav.inc file between the HEADER and the SECTION (with the class="lead").  We'll need it there for the future labs.

## Part 6: Upload your Work

When you are done with your webpage, close everything and use an FTP tool to access your account on **csc170.org** and upload your files:

- In a web browser (any), go to this address to check your handiwork:<br> **www.csc170.org/accountname/lab10**<br>(where "*accountname*" is your account name)

When you look at your Lab 10 website in your browser as it's being served from the class web server:

- All the Include statements should work on each webpage -- each page should look normal, as if the PHP includes didn't exist

...if not, you have some debugging to do. Good luck! Figure it out.

## Part 9: Report your work

- In our Blackboard section, in Lab 10, post a link to your webpage to receive credit for this Lab.