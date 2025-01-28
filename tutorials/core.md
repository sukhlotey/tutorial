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

### Workflow and Automation

**Workflow**: Automates processes by defining states, transitions, and actions for DocTypes.

**Auto Email Reports**: Sends periodic reports to users via email.

**Scheduler**: Handles background jobs and periodic tasks using the Frappe Worker.
Logging and Monitoring

**Error Logs**: Captures and displays errors for debugging.

**Activity Logs**: Tracks user activities like logins, updates, and deletions.

**Versioning**: Maintains a history of changes made to records (audit trail).
Notifications

**Email Alerts**: Sends notifications based on specific triggers or conditions.

**Notification Settings**: Allows users to manage their notification preferences.

**In-App Notifications**: Provides real-time updates within the system.
Search and Navigation

**Global Search**: Quickly searches across all DocTypes and records.

**Quick Actions**: Provides shortcuts for frequently used commands or actions.

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

