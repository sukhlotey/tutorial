# workflow-frappe

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

