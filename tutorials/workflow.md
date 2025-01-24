# Frappe Workflow

#### Workflow
In the Frappe framework, a "workflow" refers to a series of defined steps or stages that a document or 
record goes through within a business process, typically involving multiple levels of approval, 
<mark>where users with specific roles can take actions like approving or rejecting a request, allowing 
for streamlined management of complex transactions within an application built on the Frappe framework, like ERPNext.</mark>

With workflows you can rewrite how a particular process/workflow is approved in ERPNext. <mark>You can set multiple levels of
approval for an ERPNext Workflow. To allow multiple people to submit multiple requests, for approvals by multiple users,</mark>
ERPNext requires you to fill the Workflow conditions.

##### Key points about Frappe workflows:

###### Multiple states:
A document can exist in different "workflow states" representing its current stage in the process (e.g., "Draft", "Pending Approval", "Approved"). 
###### Transition rules:
Each state can have defined transition rules that determine who can take action and move the document to the next stage based on their role and conditions. 
###### Workflow actions:
Users can perform specific actions within a workflow, like approving, rejecting, or commenting on a document, which triggers the transition to the next state. 
###### Notifications:
The system can send email notifications to relevant users when a document reaches a stage where they need to take action. 

##### Things to note when creating a workflow
I. Creating a Workflow in ERPNext essentially overrides the regular Save and Submit workflow. Thus the document will function based on your Workflow and not based on the pre-set code workflow. Hence there might be no Submit button/option if you have not specified it in the Workflow you create.
<mark>If you don't apply a Workflow to a document, and that document is submittable, then it has the default workflow with states: Draft - Submitted - Cancelled. If you are applying a Workflow to a submittable document, then those default states should be handled by the user.</mark>

II. A document cannot be canceled unless it is submitted.
III. If you wish to give the option to cancel, you will have to write a workflow transition step that says from submitted you can cancel.

IV. If fields under Update Field column are not updated, a new custom field will be created with the name you set in the 'Workflow State Field' field.

V. The “Is active” activates the workflow, only one workflow for a doctype can be active at a time. The “send email alerts” notifies the users mentioned in the workflow regarding next workflow actions.

#### Workflow Actions
<mark>Workflow Actions is a single place to manage all the pending actions you can take on Workflows.</mark>
Workflow Actions will send email notifications only if the 'Send Email Alert' checkbox is ticked in the Workflow that you've created.
![Screenshot from 2025-01-22 00-42-37](https://github.com/user-attachments/assets/cb937b5e-d251-40c5-9c51-0695aa3b597e)

- Workflow Actions will not be created for a transition to optional states.
- You can set email template for Workflow Actions on each state. The template might consist of a message for users 
  to proceed with the next Workflow Actions.

#### Workflow State
Different Workflow States may be achieved before or after applying different Workflow Actions on them. If you want to create a Workflow where there are multiple approvals from manager, senior manager, general manager, etc, you can set the states for it from Workflow States.

<mark>The Workflow States can have different colors according to the state.</mark>

* Success - Green
* Danger - Red
* Inverse - Black
* Primary - Dark Blue
* Info - Light Blue
* Warning - Orange

Document statuses:

* Saved = 0
* Submitted = 1
* Canceled = 2


![Screenshot from 2025-01-22 00-41-35](https://github.com/user-attachments/assets/763de9bb-5620-4d27-8acd-d65a3adfae9a)

I. Workflow States like Approved, Cancelled, etc.

II. These define every stage in a workflow.

III. States can be customized based on the requirement.

#### Assignment Rule

<mark>An Assignment Rule lets you set up automatic assignment of documents to Users.</mark>

**Tip:** Select the condition for the assignment. You can write simple Python expressions for automatic assignment in the Assign Rule, Close Rule and Unassign Rule. You will have access to all the properties of the document and can use operators like >, <, ==, etc and also multiple conditions like and and or. 

* <mark>You can also set up multiple auto assignments for each Document Type, the one with the highest Priority will be applied first.</mark>

**Example:** 
* <code> status == "Open"</code>
* <code>issue_type == "Technical" and priority=="High" and status == "Open" </code>

**Select assignment rule:**

I. Round Robin: Assign each document to a User in sequence.
II. Load Balancing: Assign new documents to the User who has the least number of assignments.

**Setting due date for assignment**

<mark>You can auto set due dates for assignments based on the date field in the reference document.</mark>

**Note:** "Due Date Based On" option will not be available if "Document Type" is not yet selected or if the selected Document Type does not have any "Date" or "Datetime" field.
