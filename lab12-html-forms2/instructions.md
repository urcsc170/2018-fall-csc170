# Lab 12: HTML Forms, Part 2
*Due: Tuesday, November 6, 2018 (one week)*

For this lab you will integrate the non-working HTML form from Lab 11 into your lab website and power it with a PHP script.

## Step 1: Copy Lab 10

- Make a copy of your Lab 10 (*not Lab 11!*) - put it in a folder named **lab12**

## Step 2: Create a New Webpage for your HTML Form

- Make a duplicate of one of your existing webpages - any of them *except* start.php - name it: **contact.php**
- Edit the new **contact.php** file:
  - Delete the ARTICLE and ASIDE and all their contents
- Get your Lab 11 file, **contact.html** and copy-out the FORM element (all of it, from the opening FORM tag to the closing FORM tag) and paste it into the new **contact.php** file, under the *nav.inc* statement
- Edit your **inc/nav.inc** file:
  - Add a list item to the new **contact.php** file
  - Have the text for the link say something like "Contact Us" ...or something like that
  - Save and close the **inc/nav.inc** file

## Step 3: Add Styles to the HTML Form

- Edit the **contact.php** file:

  - In the opening FORM tag change the **action="#"** attribute to:<br> `action="form-processor.php"`
  - Add `class="full-width"` to the opening FORM tag

- Edit the **css/styles.css** file:

  - Add a class named **.full-width** to the group selector that sets the grid-column to 1/3 like this...

    ```css
    header, footer, .lead, nav, .full-width {
    	grid-column: 1 / 3;
    }
    ```

- Save and close the **css/styles.css** file

- Edit the **inc/html-top.inc** file:

  - Change the TITLE to say "Lab 12..." instead of Lab 10

  - Add a new LINK to a new stylesheet (that you'll create next) like this

    ```css
    <link rel="stylesheet" href="css/forms.css">
    ```

- Save and close the **inc/html-top.inc** file

- Create a new file in the **css** folder named **forms.css**

- Edit the new **css/forms.css** file

  - Here you can add whatever styles you want to make your HTML form look like it's a part of your website.  At the bare minimum, try these styles...

  ```css
  form { 
  	margin-top: 30px;
  }
  textarea {
  	width: 100%;
  	height: 100px;
  }
  ```

  ...do more as you'd like.  (Not graded.)

- Save and close the **css/forms.css** file


## Step 4: Create the Form Processor File

- Make a duplicate of one of your existing webpages - any of them *except* start.php or contact.php - name it: **form-processor.php**

- Edit the new **form-processor.php** file:

  - Delete the ARTICLE and ASIDE and all their contents

- Under the *nav.inc* statement, add a MAIN element with an attribute: `class="full-width"` and add some content like this:

  ```html
  <main class="full-width">
    <h2>Thank You <?php echo $name; ?></h2>
    <p>Go back to <a href="contact.php">the contact page</a>.</p>
  </main>
  ```

  ...notice the variable `$name` used above.  That assumes you created a variable like that in your PHP script.  If not use whatever YOU used.  (E.g. maybe you called it, "fullname" or something like that?)

## Step 5: Add and Edit the Form Processing Script

- Download the ZIP'd file: [form_processing_script.zip](http://csc170.org/rkostin/distribution/form_processing_script.zip) and extract the text file 
- Copy all the text out of that file (112 lines) and paste it in the TOP of your **form-processor.php** file, *above* the PHP **inc/html-top.inc** statement on Line 1
- Fill-in the blanks in the PHP form processor as demonstrated in the last lecture 
  - Make sure the superglobals match your `name=""` attributes from your HTML form exactly (remember: case sensitive!)
  - Create variable names for the incoming data that make sense; typically you can use the same word(s) you used in the superglobals, for example `$name = $_POST['name'];`
- Save and close the **form-processor.php** file

## Step 6: Upload, Test and Report your Work

Remember: even though you may be  running a local webserver (WAMP or MAMP) the PHP `mail()` command *won't* work because you don't have a mail server on your computer.  You can only test your **contact.php** file when it's running on the class web server.

- FTP your **lab12** folder to the class webserver 
- In a web browser test the **contact.php** page:<br> **www.csc170.org/accountname/lab12/contact.php**<br>(where "*accountname*" is your account name)
- After filling out the web form, pressing the submit button should take you to your **form-processor.php** webpage where you'll see the "Thank you " ...with the name you typed in the previous webpage there.
- A few seconds later, you should receive an email with the contents of your labels and web form data
  - If not, check your **lab12** folder for the existence of a file named **error_log**; open it and read it.  It will point you to the location(s) in your form processor where there is a mistake.
- If it's all working as expected, go to our CSC 170 section of Blackboard, and in Lab 12, post a link to the **contact.php** webpage to receive credit for this Lab.

