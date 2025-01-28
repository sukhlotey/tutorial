# Module: Automation 

### Automation
In the Frappe framework, the "automation module" refers to a set of features that allow users to configure and 
automate repetitive tasks within their custom applications, including functionalities like assignment rules, 
auto-repeat functions, milestone tracking, and event streaming, essentially streamlining complex business 
processes by reducing manual interventions and improving overall efficiency. 

###### Common automation features:
**Assignment rules:** Automatically assigning tasks to specific users based on defined criteria. 

**Auto-repeat:** Setting up recurring tasks to execute at predetermined intervals. 

**Milestone:** Monitoring progress through different stages of a process. 

**Event streaming:** Triggering actions based on specific events happening within the system. 

### Assignment Rule
An Assignment Rule lets you set up automatic assignment of documents to Users.

### Auto Repeat
Auto Repeat feature helps you create certain documents automatically in a given time period.

**From version 12,** you can Customize any Form to make the documents repeatable.

**For Example:** Assuming that you follow deferred expense system for some items.
It requires you to create same Journal Entry every month to credit Deferred Expense account 
and debit Expense Account. You can create first Journal Entry manually for it, and then create 
auto-repeat transaction for it.

### Milestone Tracking
* You can automatically track milestones based on the lifecycle of a document if it undergoes multiple stages.
* The configuration for Milestone setting can be set in Milestone Tracking and each milestone is updated in Milestone
* **Note:** A milestone stage can be defined by Link or Select properties.

A new Milestone record is created every time the status of any issue is changed.

**Features:**
- Milestones can be a great source for reporting and notifying. For example, if Lead Qualification is a
milestone on "Lead", milestones can help generate reports on the number of leads being qualified in a period.

- Using Milestones with Dashboards 
Used along with Dashboards, Milestones can help track the trends in milestones. For example,
if "Qualification" is tracked as a "Lead Stage", a Dashboard on Milestone filtered by Qualification will
show the trends of leads qualified.

- Using Milestones with Energy Points 
Energy Point Rules can be defined to automatically give Energy Points to users who achieve a milestone.
This can be used to incentivize action on transactions at various levels.

### Event Streaming 
Event Streaming enables inter site communications between two or more sites. 
You can subscribe to Document Types and stream Documents between different sites.

**For Example:** Consider you have more than one Company hosted on different sites, one among them is the
main site where you want to do ledger posting and on other sites, the Sales Invoices are generated. 
You can use Event Streaming in this case. For this, your child company sites can subscribe to the main 
company site for Item, Customer, and Supplier Document Types. The main Company in turn can subscribe to the 
child companies for Sales Invoices.

**Prerequisites**
Before creating an Event Producer, a common user needs to be created on both the sites which will be 
used to access the site and will act as an Event Subscriber. Make sure the user is a System Manager 
and has the necessary permissions for creation, updation, and deletion of the subscribed DocTypes.







