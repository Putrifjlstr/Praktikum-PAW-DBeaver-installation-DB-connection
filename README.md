# Praktikum-PAW-DBeaver-installation-DB-connection

DBeaver DocumentationDOWNLOAD
Version 23.0.EA
General User Guide
Installation
Application Window Overview
Views
Database Navigator
Filter Database Objects
Configure Filters
Projects View
Project Explorer
Query Manager
Background Tasks
Database Object Editor
Properties Editor
Data Editor
Navigation
Data View and Format
Data Filters
Data Refresh
Data Viewing and Editing
Panels
Managing Charts
Data Search
SQL Generation
Working with spatial/GIS data
Working with XML and JSON
Managing Data Formats
Virtual column expressions
SQL Editor
SQL Templates
SQL Assist and Auto-Complete
SQL Formatting
SQL Execution
SQL Terminal
Variables panel
Query Execution Plan
Visual Query Builder
Script Management
Client Side Commands
Export Command
Debug
PostgreSQL Debugger
ER Diagrams
Database Structure Diagrams
Custom Diagrams
Edit mode
Search
File Search
DB Full-Text Search
DB Metadata Search
Schema compare
Data compare
MockData generation
Dashboards, DB monitoring
Projects
Project security
Team work (Git)
Bookmarks
Shortcuts
Database Management
Sample Database
Database Connections
Create Connection
Edit Connection
Connect to Database
Invalidate/Reconnect to Database
Disconnect from Database
Change current user password
Connection Types
Transactions
Auto and Manual Commit Modes
Transaction Log
Pending transactions
Database drivers
Tasks
Data export/import
Data migration
Data Import and Replace
Database backup/restore
Task management
Task scheduler
Composite tasks
Sending results by e-mail
Cloud Explorer
AWS
AWS Credentials
AWS SSO
GCP Credentials
GCP SSO
Enterprise Databases support
MongoDB
Cassandra
InfluxDB
Redis
AWS (Amazon Web Services)
DynamoDB
DocumentDB
Keyspaces
GCP (Google Cloud Platform)
Bigtable
Couchbase
Apache Hive/Spark/Impala
Oracle
Customizing DBeaver
Changing interface language
Installing extensions - Themes, version control, etc
DBeaver Enterprise
Enterprise Edition
Troubleshooting
Command Line
Reset UI settings
Reset workspace
Troubleshooting system issues
Posting issues
Log files
JDBC trace
Thread dump
Admin Guide
Managing connections
Managing variables
Managing drivers
Windows Silent Install
Snap installation
License management
License Administration
How to Import License
How to Reassign License
Tutorials
Connecting to Oracle Database using JDBC OCI driver
Importing CA Certificates into DBeaver
Create Connection
DBeaver provides a wizard that guides you through the steps to create a connection. If you run DBeaver for the first time (standalone version), the new connection wizard appears automatically. In other cases, to create a connection, do one of the following:

Click the New Connection Wizard button in the application toolbar or in the Database Navigator view toolbar:



Click Database -> New Connection in the menu bar:



Press Ctrl+N or click File -> New in the menu bar:


Then, in the wizard, click Database connection and then click Next:



Then, in the Create new connection wizard:

Choose a driver for the new connection: click the name of the suitable database type in the gallery. Then click Next.



To quickly find the needed driver, you can type a hint in the text field above the list of drivers.
If you cannot find a driver for your database then probably there is no suitable driver and you need to create one. Please see Database Drivers article.

NOTE: The list of database drivers diaplays the number of exising connections next to each driver. No number is displayed if there are no connections.

If you prefer the classic list view of the available drivers, use the Classic button.



You can choose the Simple mode on this step. Simple mode gives simplified access to the database, which is basically with the ability to view data only in schemas and tables.



In the Connection Settings screen, on the General tab, set all primary connection settings:



For most drivers required settings include:

Host
Port
Database name
User name and password
However, the number and type of connection properties are very dependent on the driver.
For example, embedded drivers (such as SQLite, Derby Embedded, HSQLDB, H2 Embedded), unlike remote ones, require only the path to the database.

If necessary, specify advanced settings, see Advanced Settings section below, and click Next.

To test if the connection works, click Test Connection.
Click Finish. The connection appears in the tree of connections in the Database Navigator and DBeaver actually connects to the database.
Advanced Settings
Network Settings (SSH, SOCKS, SSL)
If your database cannot be accessed directly, you can use SSH tunnel:



DBeaver supports following SSH authentication methods: user/password, public key authentication and agent authentication. Supported implementations for agent authentications are pageant and ssh-agent.

If a connection has network settings specified, such a connection appears in the application with a special 'arrow' icon such as this: 

More information about SSH configuration can be found on SSH configuration page.
Connection Details (name, type, etc.)
You can also set the connection name, type and initial settings (such as bootstrap queries, transaction state, global filters, etc.).



Driver Properties
Each driver has its own set of additional properties. Refer to the driver documentation to get information about available properties and their values.



Variables in parameters
You can use variables in all connection parameters and in the driver properties. Variables are system environment variables or one of the following list:

Name	Value
${host}	Host name
${port}	Port number
${database}	Database name
${server}	Server name
${url}	Connection URL
${user}	User name
${password}	User password
Note: option Use environment variables in connection parameters must be turned on (see preferences).
