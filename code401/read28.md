# Django CRUD and Forms


## Overview

**An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server. Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on. Forms are also a relatively secure way of sharing data with the server, as they allow us to send data in POST requests with cross-site request forgery protection.**

**While we haven't created any forms in this tutorial so far, we've already encountered them in the Django Admin site — for example, the screenshot below shows a form for editing one of our Book models, comprised of a number of selection lists and text editors.**


## Django form handling process

**Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models): the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed). What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.**

**A process flowchart of how Django handles form requests is shown below, starting with a request for a page containing a form (shown in green).**


![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png)



> **Based on the diagram above, the main things that Django's form handling does are:**

- Display the default form the first time it is requested by the user

- Receive data from a submit request and bind it to the form

- Clean and validate the data.

- If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.

- If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)

- Once all actions are complete, redirect the user to another page.



> **The arguments that are common to most fields are listed below (these have sensible default values):**

- **required**: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.

- **label_suffix**: By default, a colon is displayed after the label (e.g. Renewal date:). This argument allows you to specify a different suffix containing other character(s).

- **initial**: The initial value for the field when the form is displayed.


- **widget**: The display widget to use.


- **help_text (as seen in the example above)**: Additional text that can be displayed in forms to explain how to use the field.


- **error_messages**: A list of error messages for the field. You can override these with your own messages if needed.

- **validators**: A list of functions that will be called on the field when it is validated.

- **localize**: Enables the localization of form data input (see link for more information).

- **disabled**: The field is displayed but its value cannot be edited if this is True. The default is False.



## Validation


***Django provides numerous places where you can validate your data. The easiest way to validate a single field is to override the method clean_<fieldname>() for the field you want to check. So for example, we can validate that entered renewal_date values are between now and 4 weeks by implementing clean_renewal_date() as shown below.***


## The template

Most of this will be completely familiar from previous tutorials. We extend the base template and then redefine the content block. We are able to reference {{ book_instance }} (and its variables) because it was passed into the context object in the render() function, and we use these to list the book title, borrower, and the original due date.

The form code is relatively simple. First, we declare the form tags, specifying where the form is to be submitted (action) and the method for submitting the data (in this case an "HTTP POST") — if you recall the HTML Forms overview at the top of the page, an empty action as shown, means that the form data will be posted back to the current URL of the page (which is what we want!). Inside the tags, we define the submit input, which a user can press to submit the data. The {% csrf_token %} added just inside the form tags is part of Django's cross-site forgery protection.



### Other ways of using form template variable

> **It is also possible to have complete control over the rendering of each part of the form, by indexing its properties using dot notation. So, for example, we can access a number of separate items for our renewal_date field:**

- {{ form.renewal_date }}: The whole field.

- {{ form.renewal_date.errors }}: The list of errors.

- {{ form.renewal_date.id_for_label }}: The id of the label.

- {{ form.renewal_date.help_text }}: The field help text.





