# Module: Website

### Website
Websites are a core component of any business. Having a good website usually means running into 
obstacles like investing a lot of money, difficult to update, and it not being interactive.

If you're not a web designer yourself, wouldn't it be nice if there was a way to update the product 
catalog on your site automatically from your Frappe? We thought exactly the same thing and hence built 
a small Website module right inside Frappe! Using this module, you can:

* Create Web Pages
* Write Blogs
* Publish your Product Catalog using the Item master
* Allow users to buy your products using the Shopping Cart

You need to use html\css to make better custom website designs. Though not necessary, to make a good website, 
you might have to know a bit of HTML/CSS or hire the services of a professional. 
The good part is that once this is set up, you can add and edit content, blogs, 
and products directly from your ERPNext account.

#### Web Page

Static Content like your Home Page, About Us, Contact Us, Terms pages can be created using the Web Page.

* Go to the Web Page list and click on New.
* Enter a Title and add content in Main Section. The route will auto generated but you can change it.
* Click on Save.
* The web page will be published only when Published is ticked.

![Screenshot from 2025-01-28 17-28-28](https://github.com/user-attachments/assets/d921147b-7dea-46ea-bd7e-39749fcff0d3)

View your Web Page by clicking on See on Website in the side bar.

![Screenshot from 2025-01-28 17-25-58](https://github.com/user-attachments/assets/92141bd5-1c3a-482e-8e4c-7a20fec0c2ff)

### Tips on making a good Web Page

#### Title

The first thing to set is the title of your page. The title has the maximum weight for search engines so choose 
a title that reflects the keywords that you are targeting for your audience. The route (URL) will be 
auto-generated from the title but you can change it.

#### Content

You can write your content in Rich Text, Markdown or HTML. If you want to make simple content pages, 
Rich Text and Markdown are great options.

#### Images

For Rich Text Content, you can directly embed images using the editor. For Markdown and HTML, 
you must attach the images to the document first. Now get the URL of your image by right-clicking 
on your attachment and copying the address.
![image](https://github.com/user-attachments/assets/ad86d54a-7c08-4ecc-8461-f3bdc575217f)

#### Features
The Web pages provides web templates:

##### Slidesshow
You can also add a Slideshow to your Web Page.

* Choose the Content type **Page Builder**
* Add row
* Select Slideshow
* Upload Image and add title and content

![slides](https://github.com/user-attachments/assets/b593e774-33dd-4a32-aedf-8aa4d8b85372)

##### Scheduled Publishing
You can schedule your Web Pages for publishing if you set Start Date and End Date for your Web Page. They will be set as published within the date ranges and will be unpublished outside the range automatically.
Unpublished pages will throw an Error 404 when they are visited.
![Screenshot from 2025-01-28 17-49-58](https://github.com/user-attachments/assets/dec428cd-0c5f-47ee-8c2d-5ea9b0a13a82)

##### Sidebar

You can add a Website Sidebar with custom links on your Web Page. In the Sidebar and Comments section enable Show Sidebar. Select an existing Website Sidebar or create a new one.
![Screenshot from 2025-01-28 17-54-34](https://github.com/user-attachments/assets/28279ba7-a353-4722-9fa7-4c2a4de35572)

Add links and their route in the Sidebar Items table.

![Screenshot from 2025-01-28 17-55-00](https://github.com/user-attachments/assets/74cd652c-af71-4c34-bce2-1c90f11cd684)

![Screenshot from 2025-01-28 17-57-13](https://github.com/user-attachments/assets/f07a5ea2-7418-47c2-81e6-475ccf87cc59)

##### Header
You can add a custom HTML for the header section of the page. This will override the title of the Web Page.

##### Breadcrumbs
You can add a list of breadcrumbs on your Web Page. These will be shown on top before the header.
![Screenshot from 2025-01-28 18-01-56](https://github.com/user-attachments/assets/4b9b6c7f-eda8-4b82-ba1d-75ae2939f151)

![Screenshot from 2025-01-28 18-02-20](https://github.com/user-attachments/assets/a5aa30f7-8726-4264-a313-57cc8916803f)

### Blog Post

A Blog Post is an article on your website.

Blogs are a great way to share your thoughts about your business. It helps keep your customers and readers updated on news related to your business.

In the age of the internet, writing assumes a lot of significance because when people come to your website, they want to read about you and your product.

#### How to create a Blog Post 

* Go to the Blog Post list and click on New.
* Enter the Title, Blog Category, Blogger, and the Content.
* Enable Published and click on Save.

![Screenshot from 2025-01-28 20-36-59](https://github.com/user-attachments/assets/92075a40-03d0-4a2e-94a7-d54caa09bdb7)

Preview

![Screenshot from 2025-01-28 20-38-09](https://github.com/user-attachments/assets/6f68899c-77c7-4770-9d1f-856f23eeaaf8)

Check the Disable Comments option if you'd like to disable the ability for readers to add comments to the current blog post.

![Screenshot from 2025-01-28 20-43-19](https://github.com/user-attachments/assets/11cc2b38-3717-41d7-8441-0c3292c5eb53)

#### Features

##### Blogger
Blogger is a user who can post blogs. To create a Blogger, go to:

Home > Website > Blog > Blogger.

You can mention a short bio about the blogger and also set an avatar here.

![image](https://github.com/user-attachments/assets/de86d9cf-f35b-4914-b77e-055defb91d81)

#### Web Forms

Stakeholders who are not part of your organization may need to interact with your Frappe instance. You can authorize customers, suppliers, job applicants, students, and guardians to access certain information or even create certain transactions. For example, you can let anyone create an account on your website (created with Frappe) and apply for a job. You can let your customers see the details of the complaints they have registered. These can be done using Web Forms.

To create a new Web Form go to:

Home > Website > Web Site > Web Form

Here is an explanation of each of the checkboxes on the right.

* Published: Web Form will be accessible only if this is enabled.
* Login Required: User can fill the Web Form only if they are logged in. When Login Required is checked,
* Route to Success Link: Go to Success Link after the form is submitted.
* Allow Edit: If this is unchecked the form becomes read-only once it is saved.
* Allow Multiple: Allow user to create more than one record.
* Show as Grid: Show records in a table format.
* Allow Delete: Allow user to delete the records that he/she has created.
* Allow Comments: Allow user to add comments on the created form.
* Allow Print: Allow user to print the document in the selected Print Format.
* Allow Incomplete Forms: Allow user to submit form with partial data.

![Screenshot from 2025-01-28 21-01-02](https://github.com/user-attachments/assets/d4c93fec-f80e-488a-8a36-7ca420e6622b)

#### Web Page Builder
Page Builder lets you quickly create web pages from pre-configured web templates.

* How to create a page using Page Builder 
* Follow the steps to create a Web Page.
* Enable full width by ticking the "Full Width" checkbox.
* Select Content Type as Page Builder.
* Click on Add Row in the Page Building Blocks Table.
* Select a Web Template.
* Click on the Edit Values button.
* Enter values in the dialog and click on Submit.
* Click on Save.
* The web page will be published only when Published is ticked.

![Screenshot from 2025-01-28 21-08-46](https://github.com/user-attachments/assets/6c131bad-c124-4a9d-80cf-84e7968a2908)

Preview of full width image

![Screenshot from 2025-01-28 21-09-24](https://github.com/user-attachments/assets/32167a01-fb31-4c72-b1dc-97e8cb4c0a84)






