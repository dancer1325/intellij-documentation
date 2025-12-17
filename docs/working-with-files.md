[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-files.html)
[//]: # (Downloaded: 2025-12-17 20:07:24)

# File management

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




To run your statements and keep track of your code ideas, use the Database Tools and SQL plugin's special file types. You can also work with the files that you store on your machine, and edit the DDL of database objects in the IntelliJ IDEA internal files.

  * Query files are SQL files that are attached to a particular data source. When you create a data source, a query file is created automatically. But you can add more query files to a data source, each of them will then create a new connection. If you do not want to create new connections, enable [single session mode](configuring-database-connections.html#enable-single-session-mode). By default, query files are located in the .idea/queries directory . For more information about query files, refer to [Query files](query-files.html).

  * Scratch files are similar to query files, but they are not attached to a data source. We refer to scratch files as temporary notes or drafts for code ideas. Usually, scratch files are outside of the project context. But you can associate an SQL scratch file with a data source and use it as an SQL editor. For more information about scratch files, refer to [Scratch files](scratches.html). 

  * User files are SQL scripts that you store on your computer or on a server. For more information about working with directories and user files, refer to [User files](working-with-user-files.html).

  * Object editors are internal files where you edit the DDL of a procedure, a view, a function, or other objects.




| Context| Functionality  
---|---|---  
Query files| Executable SQL files that are attached to a specific data source.| 

  * Files that you can use to compose and execute SQL statements in the project context.
  * Query files are attached to a data source.
  * Default resolve mode is [Playground](query-files.html#resolve_mode_playground).

  
Scratches| Files that are not attached to a specific data source.| 

  * Temporary notes or drafts for your code outside the project context.
  * By default, scratch files are not attached to a data source.
  * Default resolve mode is [Script](query-files.html#resolve_mode_script).

  
User files| Files that are stored on your machine.| 

  * Can be opened from different projects.
  * Can be put under [Version Control](version-control-integration.html).
  * By default, user files are not attached to a data source.
  * Default resolve mode is [Script](query-files.html#resolve_mode_script).

  
  
To execute statements from a scratch file or a user file, select a data source from the <data source> list.

To have a correct resolve in the user files that you do not attach a query file to, map the SQL files to any [resolution scope](settings-languages-sql-resolution-scopes.html) in Settings | Database | SQL Resolution Scopes.

10 December 2025

[Data loaders](data-loaders.html)[Query files](query-files.html)
