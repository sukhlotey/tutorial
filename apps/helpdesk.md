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
