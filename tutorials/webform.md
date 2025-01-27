# Tools: Web Form

### Web Form

Frappe provides an easy way to generate forms for your website with very little configuration. 
These forms may be public (anyone can fill them up) or can be configured to require login.

![Screenshot from 2025-01-27 16-36-28](https://github.com/user-attachments/assets/7c506441-0ac1-4d3a-b73e-a076d2f2120e)

### Creating a Web Form 

To create a Web Form, Go to:

Home> Website> Web form> +Add Web Form

* Enter Title
* Select DocType for which the record should be created.
* Add some introduction (Optional).
* Click on "Get Fields" button to get all fields from selected doctype OR select fields for your web form.
* Publish it and you are good to go.

![Screenshot from 2025-01-27 16-11-08](https://github.com/user-attachments/assets/61c7b49d-c08e-4344-b5d6-8b9deef5fbc8)

#### Fields

![Screenshot from 2025-01-27 16-11-32](https://github.com/user-attachments/assets/35f09ce1-dd7c-4cc2-b0f6-316a29b0fe82)

#### Standard Web Forms

If you check the "Is Standard" checkbox, a new folder will be created in the module of the Web Form. 
In this folder, you will see a .py and .js file that you can use to configure the web form. 
These files need to be checked into version control with your custom app. 
You can install this app on any site and it will have this web form installed.

**Is Standard field will only be visible when you are in developer mode.**

### Settings

There are multiple checkboxs in the Settings tab that can be used to enable and disable different functionalities.

#### Login Required

If you want responses from guest user, just disable the login_required checkbox. Logged In users can also use it. It is disabled by default.

If you only want responses from logged in user just enable the login_required checkbox.

#### Allow Multiple Responses

It is used to enable users to give multiple responses which they can see in Webform List View

#### Allow Editing After Submit 
It will allow user to edit there submitted responses.

#### Allow Delete 
It will allow user to delete there submitted responses from Webform List View.

#### Anonymous 
By setting this the response received will be anonymous.

#### Apply Document Permission 
By default if user has read access to the documents submitted by different users it will be visible in the Webform List View. But he/she can only open the record from list view if Apply Document Permission checkbox is checked.

#### Allow Print 
It will add a print button to print the document. It will only be visible on View Mode.

#### Allow Comments 
It will add comment section below the webform where users can communicate. All the comments will be linked to the document.

#### Show Attachments 
It will show all the attachments attached in the document in Attachment Section.

#### Max Attachment Size (in MB) 
It will restrict users to attach large files.

#### Allow Incomplete Forms 
It will allow submission of forms even if mandatory fields are not populated.

### List Columns

![Screenshot from 2025-01-27 16-57-17](https://github.com/user-attachments/assets/2fcfffdf-2614-4430-a007-3f6e95523e85)

### Sidebar Settings

![Screenshot from 2025-01-27 16-51-07](https://github.com/user-attachments/assets/5106ecf3-5b84-4167-b8e5-d26078e65d0b)

### Customization

![Screenshot from 2025-01-27 16-12-03](https://github.com/user-attachments/assets/876cb46b-a6af-4dee-b605-eca61033b89e)

### Web Form View
![Screenshot from 2025-01-27 16-14-40](https://github.com/user-attachments/assets/e0ff2dff-7ac1-4ff1-963d-892836f20b24)

### After Submission

![Screenshot from 2025-01-27 16-15-11](https://github.com/user-attachments/assets/56815301-d7ac-4506-a775-9714d7d8c3f3)

