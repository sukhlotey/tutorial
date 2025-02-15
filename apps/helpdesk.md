# Apps: Helpdesk

### What is Frappe Helpdesk?
Frappe Helpdesk is an open source ticketing tool that helps you streamline your support workflows, handle issues
efficiently, and delight customers – all at a fraction of the cost.

### Mostly used ways:
**Frappe Cloud Helpdesk**

Hosted on Frappe’s cloud platform. Managed, secured, and maintained by Frappe.

**Self-Hosted (Local Deployment)**

Installed and run on your local machine or private server. Gives full control over customization and data.

### Steps of locally manage
**Be sure you have bench installed in your system**

##### Step: 1
* Create a new site

```bash
bench new-site myhelpdesk.localhost
```
* You will be prompted to set the MySQL/MariaDB root password and an administrator password for the site and should be in developer mode.

##### Step: 2

* Install the Frappe Helpdesk app:

```bash
bench get-app helpdesk
```
**Or**

```bash
bench get-app helpdesk https://github.com/frappe/helpdesk.git
```
##### Step: 3

* Run the Frappe development server to access the site locally:

```bash
bench start
```

##### Step: 4

* Login to site
* Home > Helpdesk

![Screenshot from 2025-02-15 13-38-10](https://github.com/user-attachments/assets/8761fa93-70a8-4313-a891-65a4d3a612aa)

* Click on _Visit Helpdesk_
* Now you can see the helpdesk portal

![Screenshot_from_2025-02-15_13-53-20_optimized](https://github.com/user-attachments/assets/f964a962-cfb7-42c2-9cbf-5b4fc1e56944)

### Components

**Ticket**

**Definition:** A record of a customer's issue, question, or request for support.

**Purpose**: Tracks the status, priority, and resolution of customer inquiries or issues.

**Agent**

**Definition**: A person responsible for handling support tickets and providing customer assistance.

**Purpose**: Ensures timely resolution of tickets and maintains customer satisfaction.

**Knowledge Base**

**Definition**: A repository of articles, guides, and FAQs to help customers and agents with common issues.

**Purpose**: Reduces ticket volume by enabling self-service support and faster issue resolution.

**Customer**

**Definition**: The end-user or organization seeking support or assistance through the helpdesk.

**Purpose**: Creates tickets for their issues and interacts with the support team for resolutions.

**Team**

**Definition**: A group of agents assigned to handle specific types of tickets or categories of support.

**Purpose**: Organizes support staff by expertise or department to improve ticket management and response times.

**Canned Responses**

**Definition**: Predefined, templated responses for common inquiries or issues.

**Purpose**: Speeds up ticket replies and ensures consistent communication with customers.

**Contacts**

**Definition**: Individuals or organizations registered in the helpdesk system with their contact details.

**Purpose**: Allows easy reference and management of customer information for personalized support.

###### Create Agents

* Helpdesk > Agents
* +New Agent

![Screenshot from 2025-02-15 14-06-59](https://github.com/user-attachments/assets/22a14f67-ea69-4e4d-b9d9-36d464d6fdcc)

* We can add multiple Agents and invite them via emails.

![Screenshot from 2025-02-15 14-08-41](https://github.com/user-attachments/assets/189d04d1-d89c-4146-b0fe-59cdac3d56d6)

* The invitation sent to the agent.

![Screenshot from 2025-02-15 14-15-10](https://github.com/user-attachments/assets/8f37f9f5-c1fc-4ee5-aae4-7493874d8819)

* Click on complete registeration button, then you will nagivate to that page and it will ask for set passoword

![Screenshot from 2025-02-15 14-16-19](https://github.com/user-attachments/assets/5265f4db-700b-491e-a629-a3535943a701)

* Now this new agent an see helpdesk portal

![Screenshot from 2025-02-15 14-22-50](https://github.com/user-attachments/assets/98693b13-9953-43e8-8513-a940e84c6c37)

###### Create Teams
* Create team so that it will assign to tickets to give answer on specific topic
* In simple we create experts of specific topics
* Helpdesk > Teams
* +New team

![Screenshot from 2025-02-15 14-32-22](https://github.com/user-attachments/assets/9de335f5-6e53-4534-8e14-54f08f87621a)

* Add members

![image](https://github.com/user-attachments/assets/67c4c186-c543-4215-8aa4-276c258007e7)

* Automate the teams. When user create a ticket the team should be auto assigned.

1. Move to desk
2. Search for server script
3. Select doctype: HD Ticket
4. Doctype Event: Before save
5. Script:


```bash
if (doc.custom_category == "GNE Team"):
    doc.agent_group = "GNE Team"

elif (doc.custom_category == "Product Experts"):
    doc.agent_group = "Product Experts"
    
elif (doc.custom_category == "Desk Team"):
    doc.agent_group = "Desk Team"

else: 
    doc.agent_group = "Billing"
```
6. Save
7. Go to HD Ticket doctype
8. Customize the form:
* Add field
* Data type: check and name: custom_category
* Add Options:

I GNE Team

II Product Experts

III Desk Team

IV Billing

9. Go to HD Ticket template
10. Add row
11. Add field _custom_category_ (required)

**Now you can see the option**

![Screenshot from 2025-02-15 14-50-02](https://github.com/user-attachments/assets/3f50ee0f-603b-4503-bd65-fe6c7bb393b3)

**Now the team will auto assigned**

##### Create Knowledge base

* Helpdesk> Knowledge base
* +Add new
* Choose category or Article
* If choose catgory then we can create many articles in one category.
* If choose artcile then it will be independent article.
* Make sure it will be published.

##### Canned Responses
* Helpdesk> Canned Responses
* +Create

![Screenshot from 2025-02-15 14-55-51](https://github.com/user-attachments/assets/f68773c7-91c8-4822-99b8-95f942589672)

**Canned responses are pre messages**

##### Add Customers
* Helpdesk> Customers
* +New Customers
![Screenshot from 2025-02-15 14-58-05](https://github.com/user-attachments/assets/e29a460a-a187-4eb2-bfea-75c9b06a1fe8)

##### Contacts
* Helpdesk> Contacts
* +New Contact

![Screenshot from 2025-02-15 15-00-29](https://github.com/user-attachments/assets/17fdd62d-23da-43ba-a9b6-c5ce3ba426a9)

##### Create Article as user


