# Module: Core

## Core

The Core module in Frappe is the backbone of the framework, containing system-level configurations,
utilities, and essential functionalities that are critical for the operation of the Frappe framework 
and any applications built on it. Below is a detailed breakdown of the Core module:

## Features

### User Management

**User**: Represents individuals who can log in to the system. Users can have different roles and permissions.

**Role**: Defines the access rights and responsibilities for users. Examples include Administrator, Manager, and Employee.

**Role Profile**: Groups multiple roles together for easy assignment to users.

**Permission Manager**: Allows granular control over which roles can access specific DocTypes and fields.

### Authentication and Authorization

**Login and Password Management:** Handles user authentication through email, password, or third-party integrations like OAuth, LDAP, or social logins.

**Two-Factor Authentication (2FA):** Provides an additional layer of security using OTPs or apps like Google Authenticator.

**Session Management:** Tracks user sessions and handles session expiry for security.

### Document Management

**DocType**: The fundamental building block in Frappe. It defines the structure of data and logic for a specific entity (e.g., Employee, Item).

**Dynamic Links**: Allows linking multiple DocTypes dynamically.

**Attachments**: Enables uploading and managing files associated with records.
Customizations

**Custom Fields**: Allows adding fields to existing DocTypes without modifying the core code.

**Custom Scripts**: Enables client-side scripting for custom logic or validation on forms.

**Customizations**: Provides tools for tailoring the system to meet specific business needs without altering the base code.
System Settings

**System Settings**: Global settings like default currency, time zone, date format, and email configurations.

**Email Domain and Email Account**: Manages email integration for notifications, communications, and alerts.

**SMS Settings**: Configures SMS gateways for sending transactional messages.

### API and Integration

**REST API:** Provides endpoints for interacting with the system programmatically.

**Webhooks:** Sends HTTP requests to external systems based on specific triggers.

**Data Import and Export:** Facilitates bulk data upload and download using CSV or Excel files.

### Multi-Tenancy and Sites

**Site Management:** Supports hosting multiple sites (tenants) on the same server.

**Site Configuration**: Manages site-specific settings in the site_config.json file.
Translation and Localization

**Translation**: Supports multi-language translations for the user interface.

**Language Settings**: Configures the default language for a site or user.
Data Security

**Encryption**: Ensures sensitive data is encrypted in transit and at rest.

**Backups**: Automates database and file backups for disaster recovery.

**Access Control**: Implements role-based and user-based access control for data and actions.
Printing and Reporting

**Print Formats:** Customizable templates for printing invoices, reports, and other documents.

**Query Reports:** SQL-based reports for advanced data analysis.

**Script Reports**: Python-based reports for complex logic.

### Queue Management

**Background Jobs**: Manages long-running tasks like email sending, report generation, and data imports.
**Redis Queue:** Uses Redis to handle asynchronous tasks efficiently.

### Cache Management

**Redis Cache:** Stores frequently accessed data to improve performance.
**Clear Cache**: Tools for clearing cached data when necessary.
### Event Management

**Hooks**: Custom functions triggered by specific events (e.g., before_save, after_insert).
**Event Streaming**: Synchronizes data between different Frappe instances.

### Developer Tools

**Bench CLI:** Command-line interface for managing Frappe sites and applications.
**Error Snapshot**: Provides detailed error information for debugging.
**Database Schema Viewer**: Visualizes the structure of DocTypes and relationships.
### Multi-Currency Support

* Handles transactions and reports in multiple currencies.
* Provides currency exchange rate management.
### Time Zone and Date Management

* Supports global time zones for users and transactions.
* Manages date and time formatting based on user preferences.

## Lets try to figure out its doctypes

#### Logs Doctypes

##### 1. Access Log
Records all login attempts, including successful and failed logins.
Stores details like IP address, user agent, and timestamp.

**Use Cases:**

* Security Monitoring: Detect unauthorized login attempts.
* Audit Trail: Track who accessed the system and when.
* Compliance: Maintain records for regulatory purposes.

##### 2. Activity Log

Captures user activities like document creation, updates, deletions, and submissions.
Logs actions performed by users across the system.

**Use Cases:**

* User Behavior Tracking: Monitor changes made by different users.
* Debugging: Identify when and how a record was modified.
* Audit & Compliance: Keep a history of critical actions.

##### 3. Data Import Log

Logs details of data imports, including success, failure, and errors encountered.

**Use Cases:**

* Troubleshooting Data Imports: Identify issues in bulk data uploads.
* Data Integrity Checks: Ensure imported data is accurate.
* Performance Monitoring: Track large data imports and their impact.
##### 4. Error Log

Captures system errors, failed API requests, and exceptions in the application.
Stores stack traces for debugging.

**Use Cases:**

* Debugging & Troubleshooting: Quickly identify system errors.
* Monitoring System Health: Detect recurring issues in the application.
* Performance Optimization: Fix slow or failing processes.
###### 5. Log Setting User

Stores log settings for specific users, defining which logs they can access.

**Use Cases:**

* Access Control: Restrict log visibility to authorized users.
* User-Specific Logging: Enable or disable logs based on user roles.

##### 6. Log Settings

Manages global log settings, including log retention policies and enabled/disabled logs.

**Use Cases:**

* Performance Optimization: Reduce log size by limiting unnecessary logs.
* Security & Compliance: Define how long logs should be stored.

##### 7. Logs To Clear

Lists logs that can be cleared periodically to free up storage.

**Use Cases:**

* Storage Management: Avoid excessive log buildup.
* Performance Optimization: Improve database performance by removing old logs.
##### 8. Patch Log

Tracks patches and updates applied to the system.

**Use Cases:**

* System Maintenance: Ensure patches are successfully applied.
* Debugging Updates: Identify issues caused by recent updates.
* Audit & Compliance: Maintain a history of system modifications.

##### 9. Scheduled Job Log

Records execution details of scheduled jobs (cron jobs, background tasks).

**Use Cases:**

* Job Monitoring: Ensure scheduled tasks are running as expected.
* Debugging Failures: Investigate failed or delayed jobs.
* Performance Analysis: Optimize long-running jobs.

##### 10. Transaction Log

Captures financial and business transactions in the system.

**Use Cases:**

* Audit & Compliance: Maintain a record of critical transactions.
* Fraud Detection: Identify suspicious financial activities.
* Business Intelligence: Analyze transaction trends.

##### 11. User Social Login

Logs social media login attempts (Google, Facebook, etc.).

**Use Cases:**

* Security & Authentication: Track login sources.
* Debugging Login Issues: Identify failed login attempts via social accounts.

##### 12. View Log

Tracks which records were viewed by which users.

**Use Cases:**

* User Activity Monitoring: Identify who accessed specific documents.
* Privacy & Security: Detect unauthorized access to sensitive records.
* Audit Trail: Maintain a history of document views.















































## Importance of the Core Module
The **Core** module is essential for:

* Setting up and managing the Frappe environment.
* Defining the structure and behavior of applications.
* Enabling seamless user experiences through robust authentication, authorization, and customization options.
* Facilitating automation, integration, and reporting for business processes.

## Summary 
The Core module in Frappe serves as the foundation of the framework, providing essential system-level 
functionalities and configurations that support all applications built on it. It manages user authentication, 
roles, and permissions, ensuring secure and efficient access control. Key features include document management
through DocTypes, system customization with custom fields and scripts, and global settings for time zones,
currencies, and email configurations.

