[//]: # (Source: https://www.jetbrains.com/help/idea/create-and-modify-dialogs.html)
[//]: # (Downloaded: 2025-12-17 19:22:51)

## Databases

The set of available properties of database objects depends on the database vendor. For more information about database-specific properties, refer to the official documentation of the database that you are working with.

For more information about databases, refer to the [Databases](databases.html) topic.

![the Create database dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_database.png)

Item| Description  
---|---  
Name| Sets a name for the database.If available, click ![the Auto Generate icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.textAutoGenerate.svg) Auto Generate for the name to be generated automatically.  
Comment| Adds a comment to the database.For more information about how to view comments in Database tool window, refer to [View Options](database-tool-window.html#view_options).  
Template| PostgreSQL-specific. Disabled by default. Defines the `IS_TEMPLATE` parameter, marking the new database as a template if enabled.  
Allow Connections| PostgreSQL-specific. Enabled by default. Defines the `ALLOW_CONNECTIONS` parameter, allowing new connections to the database if enabled.  
Tablespace| PostgreSQL-specific. Set the default tablespace for the new database.  
Owner| Defines the owner of the database.  
Grants pane| ![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), ![the Remove icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg), ![the Up icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg), ![the Down icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg)| Use these buttons to add items, remove them, and move them up and down the list.  
Left part| Defines the grantee.  
Right part| Defines the permissions.For more information about granting permissions to users and roles, refer to the [Users and roles](database-users-and-roles.html) topic.  
Preview| The pane under the Preview separator shows the statement or statements that IntelliJ IDEA will run to achieve the result you have specified using the GUI.You can both use this pane as a preview of the auto-generated SQL script, and to write and edit statements yourself.

  * To select the settings to run the script with, click ![the Settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg) Settings.
  * To close the dialog and open your SQL script in a query file, click ![the Open query in query file icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.actions.MoveTo2.svg) Open query in console.


