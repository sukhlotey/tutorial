# Command-line Tools: Bench

### Bench
**Answer:** In the Frappe framework, bench is a command-line tool used to manage Frappe applications and sites. 
It handles the lifecycle of a Frappe project, including site creation, server management, backups,
app installation, and more.

### Installation
**Answer:** Bench can be installed using Python's pip.

### List of common bench commands

##### bench init <directory-name>

Initializes a new bench (Frappe environment) in the specified directory.

**Example**: bench init my-bench
##### bench start

Starts the development server for all sites in the bench.
It runs the server on http://localhost:8000.
##### bench new-site <site-name>

Creates a new Frappe site.
You can specify a custom database name and admin password.
##### bench use <site-name>

Switches the current active site in the bench to the specified site.
##### bench get-app <app-name> <app-repository>

Downloads a Frappe app from a Git repository and adds it to the bench.

**Example**: bench get-app library_management https://github.com/frappe/library_management.git
##### bench install-app <app-name>

Installs the specified Frappe app on the current site.

**Example**: bench install-app library_management
##### bench build

Compiles static assets (JavaScript, CSS) for Frappe apps.
##### bench migrate

Runs database migrations for the current site to apply new schema changes.
##### bench update

Updates Frappe and all apps in the bench to the latest version.
##### bench backup

Creates a backup of the site’s database and files.
##### bench restore <backup-file>

Restores a site from a backup file.
##### bench config <key> <value>

Updates the common_site_config.json file with the given key-value pair.
##### bench restart

Restarts the server and worker processes for all sites.
##### bench drop-site <site-name>

Deletes the specified site from the bench.
##### bench new-app <app-name>

Creates a new Frappe app template for development.
##### bench clear-cache

Clears all caches for the current site (used to resolve issues with stale data).
##### bench enable-scheduler / bench disable-scheduler

Enables or disables background jobs (scheduling tasks) for the current site.
##### bench set-admin-password <password>

Changes the admin password for the current site.
##### bench console

Opens a Python shell for the current Frappe environment.
##### bench shell

Opens a terminal shell with the Frappe environment activated.
### Deployment & Server Management
##### bench setup nginx

Generates an Nginx configuration file for all the sites in the bench.
You can copy this configuration to /etc/nginx/conf.d/ for deployment.
##### bench setup supervisor

Generates Supervisor configuration files for managing processes like workers, web server, and long-running jobs.
Used for production environments.
##### bench setup production <username>

Sets up a production environment using Nginx and Supervisor.
Example: bench setup production sukhpreet
##### bench setup requirements

Installs the necessary packages and dependencies for Frappe and Python environments.
##### bench setup redis

Sets up Redis for caching and background jobs. Redis is often used in production environments.
##### bench reload-nginx

Reloads the Nginx configuration to apply any changes made by bench setup nginx.
##### bench restart redis

Restarts Redis services used by the bench.
### Site & App Management
##### bench remove-app <app-name>

Uninstalls and removes an app from the current site.
Example: bench remove-app library_management
##### bench install-fixtures

Installs data fixtures (predefined data like custom fields, permissions, etc.) into the site.
##### bench uninstall-app <app-name>

Uninstalls an app from the current site without deleting it from the bench.
##### bench rename-site <old-site-name> <new-site-name>

Renames a site in the bench.
Example: bench rename-site mylibrary.localhost library.localhost
##### bench create-app <app-name>

Creates a skeleton for a new app.
Example: bench create-app my_ecommerce_app
##### bench remove-site <site-name>

Removes the site completely from the bench. The database and site files are deleted.
### Environment & Maintenance
##### bench env

Activates the Python virtual environment associated with the bench.
##### bench update --reset

Resets all changes to the latest upstream version and updates the bench.
##### bench version

Displays the current version of Frappe and all installed apps.
##### bench upgrade

Upgrades the bench to a newer version of Frappe or an app (for major upgrades).
##### bench check-requirements

Checks if all system requirements are met for running the bench.
##### bench doctor

Diagnoses common issues with the Frappe bench (e.g., memory usage, long-running tasks).
##### bench enable-maintenance-mode / bench disable-maintenance-mode

Puts the site in maintenance mode (useful during migrations or updates).
### Job Scheduling & Worker Management
##### bench enable-scheduler

Enables the Frappe scheduler to run background tasks automatically.
##### bench disable-scheduler

Disables the scheduler, preventing background tasks from being executed.
##### bench schedule

Forces the execution of scheduled tasks immediately.
##### bench clear-scheduler-locks
Clears locks that may prevent scheduled tasks from running (e.g., after a server crash).

### Cache Management
##### bench clear-website-cache

Clears cached data related to website pages and static files.
##### bench clear-all-cache

Clears all caches for the current site, including Redis cache, asset cache, and database cache.
##### bench purge-all-sessions

Logs out all users and clears session data from the database.
##### bench flush-redis

Flushes all Redis caches for the bench.
### Data Import & Export
##### bench export-fixtures

Exports custom fields, properties, and other configurations from the site into the app.
##### bench import-csv <path-to-csv>

Imports data from a CSV file into the database.
##### bench export-csv <doctype>

Exports data of a specific Doctype (e.g., User, Item) into a CSV file.
### Custom Commands
##### bench execute <method-name>

Executes a specific Python method within the Frappe environment.
Example: bench execute my_app.tasks.some_function
##### bench run-tests

Runs unit tests for Frappe or a specific app.
Example: bench run-tests --app my_app
##### bench new-doctype <doctype-name>

Creates a new Doctype in the app (used for creating custom forms or data models).
### Database & Backup Management
##### bench backup --with-files

Backs up both the database and site files.
##### bench backup-all-sites

Creates backups for all sites in the bench.
##### bench partial-restore <sql-file>

Partially restores the database from a backup (e.g., only specific tables).
### Logging & Monitoring
##### bench show-logs

Displays logs for all Frappe processes (useful for debugging).
##### bench tail <process>

Continuously displays logs for a specific process (e.g., Redis, scheduler).
##### bench log <log-file>

Displays the contents of a specific log file in the bench.
