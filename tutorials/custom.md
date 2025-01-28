# Module: Custom 
# Custom

The Custom module in Frappe is designed to allow users and developers to extend the functionality of existing
applications without modifying the core codebase. This module is ideal for creating tailored solutions, 
implementing unique workflows, or integrating specific business logic to meet organizational requirements.


## Key Features of the Custom Module
### Custom Fields

* Add new fields to existing DocTypes without altering the original structure.
* Supports various field types like text, number, date, dropdown, etc.
* Fields can be set as mandatory, read-only, or hidden.

### Custom Scripts

* Write client-side JavaScript to extend or override the behavior of forms.
* Useful for implementing custom validations, dynamic field behavior, or event handling.

### Custom DocTypes

* Create entirely new DocTypes for managing unique data or workflows.
* Includes options for defining fields, permissions, and workflows.
### Custom Print Formats

* Design personalized print formats for invoices, reports, or other documents.
* Supports HTML and Jinja templating for dynamic content.
### Custom Reports

* Develop tailored reports using Query Reports or Script Reports.
* Query Reports use SQL queries for data extraction, while Script Reports allow Python-based logic.

### Custom Workflows

* Define workflows for existing or custom DocTypes.
* Specify states, transitions, and actions for automating business processes.

### Custom Permissions

* Create role-based or user-based access controls for custom fields, DocTypes, or workflows.
* Fine-tune permissions at the field level.

### Custom Apps

* Build standalone applications with unique functionalities.
* Integrate these apps with the existing Frappe ecosystem.

### Integration with External Systems

* Use REST APIs, webhooks, or custom scripts to connect with third-party systems.
* Automate data exchange and synchronization.
### Event Hooks

* Attach custom logic to predefined events like before_save, after_insert, or on_submit.
* Extend the behavior of existing DocTypes without modifying their code.

### Custom Dashboards

* Create personalized dashboards with charts, key performance indicators, and reports.
* Provide users with actionable insights tailored to their needs.

### Custom Notifications

* Set up email or in-app notifications triggered by specific events or conditions.
* Customize notification templates for branding.

### Custom Data Import/Export

* Define custom data import templates for bulk uploads.
* Export data in specific formats for integration or reporting purposes.

## Benefits of the Custom Module
**Flexibility**: Tailor the system to meet unique business needs without altering the core framework.

**Scalability**: Add new features or workflows as the organization grows.

**Maintainability**: Keep customizations separate from the core codebase, simplifying updates and upgrades.

**User Empowerment**: Enable non-developers to make basic customizations through the user interface.

## Summary

The Custom module in Frappe enables users and developers to extend and personalize the system without
modifying the core codebase. It allows the creation of custom fields, scripts, DocTypes, workflows, 
reports, and dashboards to meet unique business requirements. Users can design tailored print formats, 
set up custom notifications, and define permissions for specific roles or fields.
