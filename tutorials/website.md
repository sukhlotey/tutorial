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





