# Lab 11: HTML Forms, Part 1
*Due: Tuesday, October 30*

For this lab you will create a non-working HTML form.  Later (in Part 2) you will stitch the form into your lab website and power it with a PHP script.

## Part 1: Create a New Webpage

*NOTE: this is different than you've been doing for previous labs.  Instead of copying your previous website, this time you're just going to start from scratch with a new, empty HTML document with no content and no CSS.*

Working on your desktop or anywhere...

- Create a new, valid HTML document named **contact.html** following the HTML5 specification (doctype, HEAD, BODY, et cetera)
- Make the TITLE of the document: "Lab 11 - HTML Forms, Part 1"
- Create an H1 in the BODY of the document and make it: "HTML Forms, Part 1"

## Part 2: Create the HTML Form

Under the H1, create a \<form\> element. The \<form\> element must have two attributes:

- A **method** that has a value of `"post"`
- An **action** that has a value of `"#"`

## Part 3: Design Your Form

Before you start building the form, think about the content in your lab website.  

- [ ] You need to design an HTML form that makes sense for your website.  

  - For instance, if your content was about Shakespeare, you would have form elements ask things that relate to Shakespeare.

  - Look at the "comp" at the end of this instruction sheet for an example

### Requirements

NOTE: don't go crazy with an awesome, long HTML form.  Just use the basic HTML form elements to demonstrate that you know how to build an HTML form.  Whatever you chose to include in your HTML form, at the **bare minimum** it must contain these form types:

- [ ] Three **text input** fields
  - They can use any combination "type" for plain text such as "text", "url", "email", et cetera
- [ ] One **text area** input field
- [ ] A set of **checkboxes** - at least three
- [ ] A set of **radio buttons** - at least three
- [ ] A **fieldset** and **legend**, used appropriately
- [ ] A **submit button** with custom words (instead of the default)

Remember: for each of the above except the submit button:

- [ ] There must be a name attribute that makes sense for what it's naming
- [ ] There must be an id attribute, and all the IDs must be unique
- [ ] Each label must use the label tag and each label tag must use the for="" attribute
- [ ] Each for="" attribute must point to the ID for which it is a label

*NOTE: for this lab only, it is okay to use the `<br>` tag liberally instead of doing things properly with CSS*


## Part 4: Upload and Report Your Work

When you are done with this one webpage, close it and FTP it to your account on **csc170.org** into a folder named `lab11`

- In a web browser (any), go to this address to check your handiwork:<br> **www.csc170.org/accountname/lab11/contact.html**<br>(where "*accountname*" is your account name)
- Don't forget to also check the **W3C HTML Validator**

*NOTE: there should be nothing else in the lab11 folder - just the one HTML file*

- In our Blackboard section, in Lab 11, post a link to your webpage to receive credit for this Lab.



# Comp

Here is an example of an HTML form you might create if your lab website content was about Shakespeare.  

Note that the form is ugly, styled only with `<br>` tags, but otherwise it's semantically correct.  (We'll style it in Lab 12.)

![Figure 1](media\figure1.PNG)