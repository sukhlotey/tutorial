# Frappe Todo

### What is frappe todo?
**Answer:** The ToDo Doctype in Frappe is used for task management, allowing users to create, assign, and 
track tasks. Let's break down your questions and analyze each component in detail.

### The view of Todo in frappe:

- Open frappe app on browser
- Go to side bar

![image (1)](https://github.com/user-attachments/assets/9124a3b1-eeae-46bd-a6f2-72c77241f725)

- Home>Tools> Todo

![image (2)](https://github.com/user-attachments/assets/265a7160-c7db-4e63-81d3-d9dc239ca71d)

- Add todo

![Screenshot from 2025-03-27 23-55-34](https://github.com/user-attachments/assets/101bc04e-d864-4ea3-a27f-13ec1908a045)

### Let's breakdown everything of todo:

- **Status:** You can define the status of the ToDo. While creation, the status of the ToDo would be 'Open' by default. The user can change it to 'Closed' when the assignment is completed.
1. Helps users know whether a task is active, completed, or canceled.
2. Used for filtering and tracking task progress.

- **Priority**: You can define the Priority of this task as Low, Medium or High.
1. Helps in sorting and filtering tasks based on importance.
2. Ensures that critical tasks are addressed first.

- **Color**: You can choose to assign a color to each of your ToDos. E.g., a ToDo created as a weekly reminder for sending reports can be assigned the color Purple, whereas all the personal ToDos can be assigned the Color Yellow.
1. Provides a quick visual representation of task priority or status.
2. Helps in differentiating tasks easily in the UI.

- **Due Date:** You can add the Due Date to all the ToDos.
1. Helps users stay on schedule.
2. Used for sending reminders and tracking overdue tasks.

- **Allocated To**: In cases where you are assigning a ToDo to another ERPNext User, you can do so here.
1. Defines responsibility for the task.
2. Helps track ownership of tasks in the system.

- **Description** A text field where additional details about the task can be added.
1. Provides context and instructions for the assigned user.
2. Helps in understanding the task's objective and requirements.

- **References** Every Document in ERPNext has an option called 'Assign To' in the side-bar. Using this option, any Dcoument can be assigned to the user. The User would be assigned a ToDo simultaneously.

- **Reference Type** When a ToDo is created from another document, say a Task or an Issue, the Reference Document Type gets linked to the ToDo here. You can also choose to add a Reference Document Type manually.
1. Helps in relating tasks to specific documents like Invoices, Orders, or Projects.
3. Enables better organization and tracking.

- **Reference Name:** On assignment via another DocType, the name of the Reference DocType also gets linked over here.
1. Allows users to directly access the related document.
2. Ensures tasks are properly associated with relevant data.

- **Role:** A user role (e.g., Manager, Sales User) that is assigned responsibility for the task.
1. Assigns tasks to a specific role instead of an individual.
2. Useful for workflows where any user with a specific role can complete the task.

- **Assigned By** The user who created and assigned the task.
1. Helps track who initiated the task.
2. Useful for accountability and reporting.

### Sidebar options

- **Assigned To** A field that lists all users assigned to the task (can be multiple).
1. Enables multiple users to work on a single task.
2. Provides a collaborative task management approach.

- **Attachments** A section where users can upload related files (e.g., PDFs, images).
1. Stores supporting documents, screenshots, or references for the task.
2. Helps in keeping all task-related materials in one place.

- **Tags** Custom labels that can be assigned to categorize tasks.

1. Helps in organizing and filtering tasks.
2. Provides an easy way to classify tasks based on topics or themes.

- **Share** A feature that allows sharing the task with other users.
1. Enables collaboration by giving visibility to other users.
2. Useful for delegation and teamwork.

### Roles
By default frappe todo allows to all can create delete update share the todo.

![Screenshot from 2025-03-28 00-33-43 (1)](https://github.com/user-attachments/assets/d8f203cb-d449-4e59-af98-c8d6bae0b7ce)

### Question

#### What are the difference between Allocated to and Assign To?
**Answer:** Both "Allocated To" and "Assign To" seem similar because both deal with assigning a task to a user. However, their functionalities are slightly different:

- **Allocated To (Field)**
1. This is a backend field that stores the actual user to whom the task is assigned.
2. It is a single-user field.
3. When a task is created and assigned to someone, the system internally stores this value.

- "Assign To" (Sidebar)
1. The Assign To in the sidebar is more of a UI feature.
2. It allows multiple users to be assigned to a single task.
3. The user(s) selected in "Assign To" appear in the list and can be managed directly from the sidebar

#### Why the names are different?
- "Allocated To" is a single-user field that holds the main responsible person for the task.
- "Assign To" allows multiple users to be assigned via the sidebar UI.
- If "Assign To" allows multiple users, the system needs to store it differently, so "Allocated To" remains a dedicated single-user field.

#### Reference Type & Reference Name
These fields help to link the ToDo item with other documents in the system.

**Reference Type** This field stores the Doctype to which the ToDo is linked.

**Example**: If the ToDo is related to a Sales Invoice, the Reference Type will be "Sales Invoice".

**Reference Name** This field stores the name/ID of the specific document.

**Example**: If the task is related to a Sales Invoice with the ID "SINV-0001", then the Reference Name will be "SINV-0001".

#### Why Are These Fields There?
These fields help link a ToDo item to a specific document, making it easy to track what the task is related to.

**Example**: If a ToDo is created for approving a Purchase Order, it will have:

**Reference Type**: "Purchase Order"

**Reference Name**: "PO-0005"

This makes it easy to filter and find ToDo items related to specific documents.

#### What is the "Color" Field?
The Color field is used to visually differentiate tasks based on their status or priority.

**Purpose of Color** It provides a quick visual indicator for users.

![Screenshot from 2025-03-28 01-02-41](https://github.com/user-attachments/assets/1f13cbf0-c65e-496a-958d-f727c406bcc2)

**Can be used to represent:**
1. Priority (Red for high priority, Green for low priority)
2. Status (Blue for in-progress, Gray for completed)
3. Helps users manage tasks more effectively by scanning them based on colors.

### Sources:

- [Official todo documentation](https://docs.frappe.io/erpnext/user/manual/en/to-do)
- [Todo source code](https://github.com/frappe/frappe/tree/develop/frappe/desk/report/todo)
- [Frappe Forum todo discussions](https://discuss.frappe.io/search?q=todo)
