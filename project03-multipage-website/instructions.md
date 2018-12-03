# Project 3: Multipage Website

*Due: Thursday, December 6, 2018*

## General and Global Requirements

In this assignment, you will create a small website using your Project 2, and **three** other students’ Project 1s.  

- Each original HTML document will be its own webpage in your website.  (4 pages of content)
- You must try to maintain the integrity of each HTML document as-is.  I.e., do *not* change the HTML documents by adding content, or moving content around much.
  - There are places where you have to add content – described later in this document.  Also, it's okay to move content around to maintain consistency between pages.  You may also remove internal navigation (if any), and resize or crop images as necessary.
- Try to use as much of the CSS you created in Project 2 as a starting point for Project 3. Your goal is to use all the original CSS you started with, and only add or tweak CSS as necessary.
  - It *will be* necessary to tweak the CSS.  VERY necessary!  Good luck with that.
- You will also create a new homepage that will serve as an entry point to all the other pages. (total of 5 pages)
- There must be a common (consistent) multicolumn layout on all pages except the homepage.
  - You may use a multicolumn layout on the homepage, but it's not required.

**It is your responsibility to obtain original Project 1 documents (HTML and image files) from other students.**  

## Validation

All HTML and CSS files must validate, however there are known errors that can be excused.  If you have questions about excusable errors, contact your TA or the professor.  Also: warnings do not have to be fixed.

- Each HTML document must pass validation using the WC3 Markup Validation Service at:<br> **http://validator.w3.org**

- The  CSS must pass validation using the WC3 CSS Validation Service at:<br> **http://jigsaw.w3.org/css-validator**

## Responsive/Adaptive Design

-  Every page on the website must display properly on all devices.

  - The website design must work at browser-widths down to mobile-size (480px wide), and large desktops (1200px wide), and everything in between.
  - On small devices: there must be no horizontal scrolling and no elements that overlap their borders.
  - On desktops, there must be no paragraphs of text that stretch more than about 700px wide. 
  - On all devices and desktops, all text and images must be legible and usable.
  - All files in the file system must be less than 300 KB.
    - Remember to check your images file sizes including background images!

## Search Engine Optimized

- Every page must be optimized for search engines

  - Proper TITLE tags in the HEAD

  - Proper semantic use of HTML elements

  - Proper outline structure using H1, H2s, etcetera

  - Proper use descriptive text in all alt="" attributes in images

  - Descriptive text in all hyperlinks

- A **sitemap.xml** file must exist in the website's root (in the **/project3** folder)

- Google Analytics (the SCRIPT from Google) must be installed on every web page

## New Content That Goes on Each Webpage

Each page in your website must have the following items **in common**<br>("In common" means that these items must be identical on each page in the website)

- A banner (in a HEADER element)
- A main menu (in a NAV element)
- A footer (in a FOOTER element)
- The overall layout using CSS Grid Layout
- A "container" to keep at least some of the content constrained in some appropriate way
  - You just have to demonstrate that you know how to do it somewhere in the website

## Title tags

- Each TITLE tag in the five HTML documents must conform to a certain style. 

  - 
    The home page must follow this pattern:
    `<title>yourname, CSC 170 Project 3</title>`

## The Banner

The banner (header) typically has three parts: (#1) a logo,(#2) some big text, and (#3) some subtext, like a catch phrase.  

- The banner must contain some large text that acts as the name for the website.
  - You can have the name for the website be simply: your name, or something else if you’re feeling creative


- You can choose whether or not to design a logo.  (It would be awesome if you did.)

- 
  Here’s an example of a combo-logo which also contains big text that acts as the name of the website: ![Example logo](media\figure1.png)

- You must include a catch phrase.  If you’re not feeling creative, at the very least, you can use this:<br> *CSC 170 - Web Design and Development*

### Banner Requirements

-  The banner must be wrapped in a HEADER tag.

-  The name of the website (plus the logo if you use one) must be wrapped in an H1

- The H1 (but not the catch phrase) must be wrapped in an anchor tag and linked to your homepage: **index.php**

## Main Menu

- You must have a horizontal-style main menu (navigation), and links to each page in your website.  

- The "current" page must be somehow styled differently to indicate that it’s the current page

Here is an example of a horizontal menu<br>![screen shot](media\figure2.png)<br>*Notice how the current page ("Cats" in this example) is highlighted compared to the other menu items.*  

- No matter what page the user is looking at, the main menu must answer the following two questions: (#1) where am I now?  (#2) Where can I go?  

### Main Menu HTML Requirements

- The main menu must be wrapped in a NAV tag.
- The main menu must be coded as an unordered list.
- Each list item must contain an anchor tag that links to one of the other webpages in the website.

You can use [the professor's menu-highlighter.js solution (ZIP)](http://urcsc170.org/rkostin/distribution/menu-highlighter.zip).

## Footer

-  The footer on each page (a "page footer" ...not necessarily the only footer) must contain your name and "CSC 170 Webpage Design and Development"

-  On each of the four sub-pages (all the pages except for the homepage: index), the page footer must contain a link to the location of the Project 1 from where the content came from.

- You can add other content to the page footer if you’re feeling creative, but whatever it is, keep in mind that everything in the footer must appear the same on each page.

Ideas: in the footer, you can link to your Facebook page, Twitter account, whatever. You can also use a copyright like this: ©2017 *your name*.  You can also insert a copy of the main menu in the footer.

### Footer HTML Requirements

-  The footer must be wrapped in a FOOTER tag.

# New Homepage 

- **Homepage layout:**You will create a new homepage (index) that will serve as an entry point to theother four pages.  It will have all thesame common elements (header, nav, footer and layout) as the other pages,except that it will have new content.
- **Homepage content:** The new content of the homepage must be a summary of each of the subpages
  - Your original Project 1 document, plus the other Project 1 documents you are using.  
  - You just need to write an excerpt OR maybe just use the first paragraph of each of the subpages and make it part of your homepage. 
- **Design:** Each excerpt must clearly indicate that it’s referring to a subpage, for example,each should have its own heading and some other visual clues that tell the user that they’re looking at group of excerpts that each refer to some other section in the website.
- In addition to headings for each excerpt,include embedded links that are redundant with the main nav, that also link to the subpages in your website.  
- **jQuery-Powered Slideshow:** The homepage must have a jQuery slideshow that automatically rotates through at least four images.  The slideshow must be positioned below the HEADER and NAVIGATION and above all other content.  The slideshow must be appropriately sized for the space it fills and work correctly (normally).  

  -  DONOT use giant images in your slideshow
  -  Note:it's okay to have the slide show occupy one side of the homepage and have the excerpts (below) along the other side.

Here’s an example of excerpts that lead to subpages. (Notice the text that says “Read more…”)<br>  ![screen shot](media\figure3.png)<br>*Note: using embedded images as shown in this example would be awesome, but not necessary*

# PHP Includes

- Your website must use PHP includes on every page to factor-out redundant code.  At a bare minimum, you must factor-out the NAV element. 

  - The include file(s) must be in a sub-folder named **inc**
  - When you move your NAV element into an include you must implement a solution (either PHP or JS) to fix the "current menu highlighter" that shows the user what page they're on.
    - You don't necessarily have to use [the **menu-highlighter.js** file provided by the professor](http://urcsc170.org/rkostin/distribution/menu-highlighter.zip) - you can find and implement some other solution

# Suggested Workflow

## Prepare your Project 2 HTML file

1.      Start by creating a new/empty folder named **project3**

2.      Make *a copy* of your entire Project 2.  

3.      Rename the Project 2 HTML file from index.php to something that describes its content (something like it’s H1), e.g. **mark-zuckerberg.php**

4.      In your copy of your Project 2 page, add the"common elements" described earlier in this document, restructuring the HTML as you go, as necessary.

## Register your Project 3 website with Google Analytics

5.      In Google Analytics (www.google.com/analytics),setup a new Google Analytics Account for your Project 3 site
        - The site will (eventually) reside at **urcsc170.org/accountname/project3** <br>*(where "accountname" is your account name)*
        - Find and copy the tracking code for your Project3 Google Analytics Account.


6.      Insert the tracking code for your Project 3 Google Analytics Account into the code of your HTML file.

## Add the Other Project 1 files

7.      When your copy of your Project 2 page is perfect make a copy of the HTML file.  Name the file "start.html"
8.      Hollow out the content the start.html file (not the common elements – just the content). 
9.      Make three copies of your start.html file.  Name them names that describes the content that will go in them (the content from the other students), e.g. **alan-turning.html**, **tim-wu.html**, and **biz-stone.html**
10.      Fix the common navigation links so they all work correctly.
11.      Carefully copy HTML content from the other students’ HTML pages.  Be sure to *copy the code* from the other HTML files – not the text from a web browser.  
       - You *will* need to re-structure the other pages' outlines (the H1, H2s, et cetera) when you bring them over.
       - If you have a Project 1 that used its own internal navigation, you may remove it.
       - Other than those things, you need to use as much of the HTML from the other students without modification, as much as possible.

## Build your Homepage

12.  Make another copy of your start.html file.  Name it **index.html** and fill it with the excerpts and links as described earlier in this document.

## Generate a sitemap.xml File

13.                       Create a sitemap.xml file and insert it into the root of your website - in the **project3/** folder on the server. (You can use: **www.xml-sitemaps.com** to generate your sitemap)

## Implement PHP Includes

14.  Convert your .html files to .php files and factor-out the NAV element and anything else you want to move to separate include files.
15.  Be sure to install the **menu-highlighter.js** file to insert the "is-current" class on the appropriate menu item for each page.

Remember: after you do this step, you must use a localhost to see your files on your laptop, or upload your files to the webserver and run them there.

# Location

- 
  Your multipage web site with image(s) and CSS must be mounted on the class webserver, where you’ll create a new folder that must be exactly this:
  ​              **project3**
  …all lower case, spelled exactly like that.
- 
  The name of the homepage must be exactly this:
  ​              **index.php**  
  …all lower case, spelled exactly like that. 
- Subpage filenames can be whatever makes sense for the current page, so long as they follow standard naming conventions for webpages: all lowercase.  No spaces.  Use hyphens to separate words. E.g. for a webpage titled: "Mark Zuckerberg, CEO of Facebook", you would use "**mark-zuckerberg.php**"
- The image(s) you use must be in a sub-directory of the **project3** folder, and the sub-directory must be named **images**
- The external CSS file must be in a sub directory of the **project3** folder, and the subdirectory must be named **css**

In a web browser (any), go to this address to check your handiwork:<br> **urcsc170.org/accountname/project3** 
(where "*accountname*" is your account name)

# Report your work

To receive credit for this project: in Blackboard, in **Project 3**, post a link to your webpage.
