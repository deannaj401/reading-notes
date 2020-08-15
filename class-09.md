# Duckett HTML

## Forms

* The best known form on the web is probably
the search box that sits right in the middle of
Google's homepage.

### Types of Forms

* Adding Text
	1. text input - Used for a single line of text such
as email addresses and names.
	1. password input -  Like a single line text box but it
masks the characters entered.
	1. Text area - For longer areas of text, such as
messages and comments

* Making Choices
	1. Radio Buttons - For use when a user must select
one of a number of options
	1. Checkboxes - When a user can select and 	unselect one or more options
	1. Drop-down boxes - When a user must pick one of a
number of options from a list.
	
* Submitting Forms
	1. Submit Buttons - To submit data from your form
to another web page.
	1. Image Buttons - Similar to submit buttons but
they allow you to use an image.

* Uploading Files
	1. File upload - Allows users to upload files
(e.g. images) to a website.


* To differentiate between various pieces of inputted data, information is sent from the browser to the server using name/value pairs

* If the form control allows the user to enter text, then the value of the form control is whatever the user has typed in.

* If the form control allows you to choose from a fixed set of
answers (e.g. radio buttons, checkboxes or a drop down list),
the web page author will add code that gives each option an
automatic value.

* You should never change the name of a form control in a page unless you know that the code on the server will understand this new value.

```<form>``` - Form controls live inside a
```<form>``` element. This element
should always carry the action
attribute and will usually have a
method and id attribute too.

**action** - Every ```<form>``` element requiresan action attribute. Its value is the URL for the page on the
server that will receive the information in the form when it
is submitted.

**method** - Forms can be sent using one of
two methods: get or post.
	*get method* - the values from the forms are added to the end of the URL specified in the action attribute. this is ideal for:
		1. short forms such as search boxes
		1. retreiving data from the web server
	*post method* - values are sent in what are known as HTTP headers. you should use the post method if:
		1. it allows users to upload a file
		1. is very long
		1. contains sensative data like passwords
		1. adds info to or deletes info from a database
		
** If the method attribute is not used, the form data will be sent using the get method.

**id** - the value is used to identify the form distinctly from other elements on the page

## Text Input

```<input>``` - is used to create several different form
controls. The value of the type attribute determines what kind
of input they will be creating.



```type="text"``` - When the type attribute has a value of text, it creates a singleline text input.

```name``` - The value of this attribute identifies the form control and is sent along with the information
they enter to the server.

```size``` - The size attribute should not be used on new forms. It was used in older forms to indicate
the width of the text input

```maxlength``` - You can use the maxlength attribute to limit the number of characters a user may enter into the text field. Its value is the number of characters they may
enter.

## Password input

```type="password"``` - When the type attribute has a value of password it creates a text box that acts just like a
single-line text input, except the characters are blocked out.
They are hidden in this way so that if someone is looking over
the user's shoulder, they cannot see sensitive data such as
passwords. 

```name``` - The name attribute indicates the name of the password input, which is sent to the server with
the password the user enters.

```size, maxlength``` - carries the size and maxinput 

```<textarea>``` - The ```<textarea>``` element is used to create a mutli-line text input. Unlike other input
elements this is not an empty element. It should therefore have an opening and a closing tag. Any text that appears between the opening ```<textarea>``` and closing ```</textarea>``` tags will appear in the text box when the
page loads. If the user does not delete any text between these tags, this message will get sent to the server along with whatever the user has typed.

### Radio Buttons

## ```<input> type

```type="radio"``` - Radio buttons allow users to pick
just one of a number of options.

```name``` - is sent to the server with the value of the
option the user selects. When a question provides users with
options for answers in the form of radio buttons, the value of
the name attribute should be the same for all of the radio buttons used to answer that question. 


```value``` - indicates
the value that is sent to the server for the selected option.
The value of each of the buttons in a group should be different (so that the server knows which option the user has selected).

```checked``` - used to indicate which value (if any) should be selected when the page loads. The value of this
attribute is checked. Only one radio button in a group should
use this attribute.

** once a radio button is selected it cannot be deselected. The user can only select a different option.

## Checkboxes

```type="checkbox"``` - Checkboxes allow users to select
(and unselect) one or more options in answer to a question

```name``` - is sent to the server with the value of the
option(s) the user selects. When a question provides users with options for answers in the form of checkboxes, the value of the name attribute should be the same for all of the buttons that answer that question.


```value``` - The value attribute indicates the value sent to the server if this checkbox is checked.

```checked``` - indicates that this box should be checked
when the page loads. If used, its value should be checked.




	








https://deannaj401.github.io/reading-notes/