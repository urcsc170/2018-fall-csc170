# Lab 13: JavaScript Basics
*Due: Tuesday, November 13, 2018 (one week!)*

For this lab, you will re-incorporate your **start.php** file (and rename it "index") to have it work like a normal index (home) page for your website.  On you index page you will incorporate two JavaScript behaviors (which will be very basic, but we'll spice them up in a later lab).

## Step 0 (prep): Get Two New Identically-sized Images

Find and prepare two new images

- [ ] The two new images must be related to your website’s topic
- [ ] The two new images must have identical height and width
- [ ] The two new images must have a width dimension of no less than 200px and no more than say about 300px

Preparing identically-sized images might take some extra work using software on your PC or Mac.

- On a PC, the application “Paint” comes with Windows and will work well enough
- On a Mac, the application “Preview” has “tools” that will work well enough
- The two new images must have filenames that comport to the rules for naming web files (all lower case, no spaces)

## Step 1: Copy Lab 12

- Make a copy of your Lab 12 - put it in a folder named **lab13**
- Add the two images you created in the previous step into the **lab13/images** folder

## Step 2: Create a Home Page

- Rename your **start.php** file to **index.php**
- In the **index.php** file, directly under the *nav.inc* remove the contents of the SECTION element with the  `class="lead"` (leave the SECTION tags there - just delete everything inside it)

- Add an H2 in the SECTION element - some kind of welcome message, something like this:<br> `<h2>Welcome to The World of William Shakespeare</h2>` <br>_(It doesn’t have to say, “Welcome to….”  You can be creative here)_
- Within the SECTION element, add a FIGURE element and a DIV like this:

```html
<section class="lead">
  <h2>Welcome to The World of William Shakespeare</h2>
  <figure>

  </figure>

  <div>

  </div>
</section><!--.lead-->
```

- Edit your **inc/nav.inc** file:
  - Add a list item to the new **index.php** file
  - Have the text for the link say something like "Home" ...or something like that
  - Save and close the **inc/nav.inc** file

## Step 3: Add a Swappable Image

Continuing in the **index.php** file...

- [ ] Within the new FIGURE element, add a FIGCAPTION and an IMG tag to embed one of the new images; something like this:

```html
<figure>
  <img src="images/______.jpg" alt="_________">
  <figcaption>Some words  - you write here</figcaption>
</figure>
```

…In the blanks (above) use whatever you named one of your new images in the SRC and write its description in the ALT

- [ ] Add the JavaScript **onmouseover** event to the image element to change the source (the “src”) to the other new image when a mouse hovers over that element


  ```html
  <img src="images/_____.jpg" alt="_____" 
       onmouseover="src='images/_____.jpg';">
  ```

  ...note that you can break this long statement into multiple lines to make it more readable<br>...beware of the single-quotes inside the double-quotes - it's important!

- [ ] Add another JavaScript **onmouseout** event to the *same image element* to change the source (the “src”) to back to the original image when the mouse moves *out* from hovering over that element


  ```html
  <img src="images/_____.jpg" alt="_____" 
       onmouseover="src='images/_____.jpg';"
       onmouseout="src='images/_____.jpg';">
  ```
  ...again, beware of the single-quotes inside the double-quotes

Test the JavaScript events in a web browser.  When you load the index file into your web browser, you should see an image.  When you hover your mouse over it, it should change.  When you move your mouse away, it should change back to the original image.

## Step 5: Add Some Hidden Content

Still editing the **index.php** file...

- [ ] Insert two DIV elements within the DIV after the FIGURE element like this:

```html
<div>
    <div>
       
    </div>
    <div>
        
    </div>
</div>
```

- Add a button element that says “More…” between the two DIVs like this:

```html
<div>
    <div>
       
    </div>
    
    <button>More...</button>
    
    <div>
        
    </div>
</div>
```

- “Steal” some content from your ARTICLE and/or ASIDE (in the same file, below)
  - A good candidate is some “Introduction” content if you have one
  - You need at least two paragraphs with headings; insert the two paragraphs (and their headers preferably) into the two DIVs (respectively); something like this (using your content, not Shakespeare)

```html
<div>
	<div>
		<h3>About Shakespeare</h3>
		<p>William Shakespeare was an English poet...p>
	</div>
	<button>More...</button>
	<div>
		<h3>More About Shakespeare</h3>
		<p>His extant works, including...</p>
	</div>
</div>
```

- Delete the rest of the content on the page: the ARTICLE, ASIDE, and FOOTER 
  - Delete not only the contents of those elements, but the elements themselves.

From an appearance standpoint, you should have something that looks like this:

![screen capture](media\figure1.png)

...when you hover your mouse of the image, it should change.  When you move your mouse away, it should change back.

### Power the 'More...' Button

Continuing to edit the **index.php** file

- Add an ID to the BUTTON element
- Add an ID to the second DIV element (directly below the BUTTON element)
- In the file system, add a new folder named: **js**
- Create a file in the **js** folder named **scripts.js**
- Near the bottom of the Index page, just above the closing BODY tag, add an embedded JavaScript block using the `<script>` tag to connect the external JavaScript file named: **js/scripts.js**

Edit the **scripts.js** file.  Add this starter code:

```js
//	*******************************************************
//	Toggle element to hide/show
//	*******************************************************

var toggle_button = document.getElementById("___________");
var toggle_element = document.getElementById("___________");

toggle_element.style.display = 'none';

function toggleElement(e) { 
	if (e.style.display == 'inline') {
		e.style.display = 'none'
	} 		
	else {
		e.style.display = 'inline'
	}
}; 

toggle_button.addEventListener("click", function(){
	toggleElement(toggle_element);
});
```

- Replace the blanks in lines 5 and 6 with the IDs that you used in the BUTTON and the DIV directly below it

## Step 6: Upload, Test and Report your Work

If your home page works correctly:

- When you first load the webpage the second paragraph is NOT showing
- When you hover your mouse over the image, it changes
- When you move your mouse away from the image, it changes back
- When you click the “More…” button, the hidden paragraph appears
- When you click the “More…”button again, the paragraph disappears again

When you are done with your webpage, close everything and use an FTP tool to access your account on **csc170.org** and upload your files:

In a web browser (any), go to this address to check your handiwork: 

**www.csc170.org/accountname/lab13/index.php**<br>(where “*accountname*” is your account name)

- Make sure the HTML and CSS pass their respective validators.
- In our CSC 170 Blackboard section in the Lab 13 assignment, post a link to your webpage to receive credit for this Lab.

