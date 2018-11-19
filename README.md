# BootstrapAssignment
Starter Code for the Bootstrap Assignment.  This assignment illustrates how to use Bootstrap to create a modal dialog box.  Modal dialog boxes are an alternative to the tradtitonal web application method of using a link to open a separate page for each page of the app.  You may find this technique useful in developing your semester project.

**Note:** The following exercise is adapted from your textbook. The exercise has been updated to use the latest version of Bootstrap, Bootstrap 4.  The major change is that Bootstrap 4 no longer provides the Glythicon font of icons.  This exercises use icons provided by Font Awesome.

## Directions

1. Create a GitHub repo for the assignment by using the link in the email you received.
2. Clone the assignment repo as a local repo.
3. Checkout the development branch.
4. Modify the code as directed below.
  * Open the index.html file.  Note that the Bootstrap and jQuery are linked through a CDN.  Note the integrity and crossorgin attributes. The integrity attribute provides a hash code that is used to ensure the libray you load has not changed from the one published.  This is called a *check code* and is implemented using a hash tequnique called SHR 256.  You should do some reading about hash codes in the SHR family.
  * Note the links to the Bootstrap CSS and the Font Awesome CSS.
  * To create the Modal Dialog, we must add the Bootstrap code to create a hidden dialog.  Start by adding the following div at the comment in the HTML code.
  
```html
<div class="modal fade" tabindex="-1" role="dialog" id="myModal">
</div>  
```
  * Inside the div you just added, add the following div to create the actual modal dialog.
  
```html
<div class="modal-dialog"></div>
```
  * The content of the modal div is defined in three sections: a header, the content, and the footer.  Add the following code inside the modal-dialog you just created.
  
```html
<div class="modal-content">
    <div class="modal-header">
        <h4 class="modal-title">Confirm Sending</h4>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
    </div>
    <div class="modal-body">
        <p>Are you sure you want to send the email?</p>
    </div>
    <div class="modal-footer">
        <button type="button" class="btn btn-primary" data-dismiss="modal">Yes</button>
        <button type="button" class="btn btn-default" data-dismiss="modal">No</button>
    </div>
</div>
```
 * If you display the page in the browser, you should see only the email button. Clicking the email button does nothing.  Add the attributes **data-toggle="modal" data-target="#myModal"** to the email button to allow the Javascript code to display the form.  Look at the Javascript in js/email.js to see how the modal dialog is displayed.
 
5. Add the Font Awesome fa-question-circle glyphicon before the sentence that starts, "Are you sure ...".  Note that this has be done using an empty span.
 
6. Clicking the No button on the dialog box closes the dialog box.
  * Add another Bootstrap alert in the HTML like the alert with ID "yesAlert", but make the new alert use ID "noAlert".
  * Change the wording to indicate that something went wrong, and change the "ok" glyphicon to "exclamation-sign".
  * Change the alert's class from "alert-success" to "alert-danger".
  * Finally, add some JavaScript similar to the code that is already present that will register a callback function when the No button (button with the class btn-default) is clicked. The callback function should show the alert with ID "noAlert".

