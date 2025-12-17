[//]: # (Source: https://www.jetbrains.com/help/idea/glossary-database-tools-and-sql.html)
[//]: # (Downloaded: 2025-12-17 19:28:10)

# Glossary for the database management functionality

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




Connection to a database
    

To connect to a database, IntelliJ IDEA requires connection details (for example, host, port, password, SSH configuration settings, and so on). For every database, the connection details are stored in a dedicated connection configuration — [data source](managing-data-sources.html).

For a data source, connections to the database are established in special wrappers – [sessions](managing-connection-sessions.html). Each session is a wrapper over a single connection, and it stores the connection's information (for example, whether it is active or not, transaction control mode, and other settings). 

A connection within a session appears when you perform an action that requires interaction with the database.

For example, once you double-click a table under a data source in Database tool window, a new session is created, connected, and it has the [data editor](data-editor-and-viewer.html) as its client. IntelliJ IDEA requires an active connection to request the table data from the database, receive it, and display it in the data editor.

For more information about connecting to databases, refer to [Connection to a database](connecting-to-a-database.html) topic.

Data source
    

Data source is a connection configuration. It stores a list of connection details that are used to establish connection to a database. For example, host, port, database name, driver, SSH and SSL configuration settings, and so on. In data source settings, you can also select databases and schemas for introspection and display in Database tool window, and change the driver for your connection.

![Data source with connection details for a PostgreSQL database](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_details_postgresql_default.png)

You can view the list of created data sources and explore them in the Database tool window (View | Tool Windows | Database) .

![Data sources in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/data_sources_list.png)

For more information about creating a data source for the supported database vendors, refer to the [Create a data source](managing-data-sources.html#create_a_data_source) section.

For more information about managing data sources, refer to the [Data sources](managing-data-sources.html) topic.

For more information about the Data Sources and Drivers dialog, refer to the [Data Sources and Drivers dialog](data-sources-and-drivers-dialog.html) topic.

DDL data source
    

DDL data source is a virtual view of a database structure based on SQL files that contain data definition language statements (DDL statements). You can reference all tables, columns and other objects defined in such files in the editor. Diagrams are also supported.

DDL data source lets you maintain database versioning. Keep the SQL files under a VCS system and regenerate them every time your database structure is updated.

Once created, DDL data sources are available in Database tool window (View | Tool Windows | Database) . You can create and manage the SQL files with statements in the Project tool window (View | Tool Windows | Project) .

![DDL data source in Database tool window and SQL files with statements in Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/ddl_data_source_and_files.png)

For more information about DDL data sources, refer to the [DDL data sources](ddl-data-sources.html) topic.

Session
    

Each session is a wrapper over a single connection, and it stores the connection's information (for example, whether it is active or not, transaction control mode, and other settings).

Sessions can have clients – files, whose queries are sent by using the connection that the session holds. [Data editor](data-editor-and-viewer.html) can also be a client for a session.

For example, once you double-click a table in Database tool window, a new session connects to the database, and the table is attached to the session as its client.

You can view data sources, sessions, and session clients in the Services tool window. The green dot in the corner of a session's icon indicates a connected session. 

For more information about sessions, refer to [Sessions](managing-connection-sessions.html).

Data editor and viewer
    

The data editor and viewer, or data editor, provides a user interface for working with data. In the data editor, you can sort, filter, add, edit, and remove the data as well as perform other associated tasks.

In IntelliJ IDEA, the data editor and viewer lets you work with database object data, query result sets, and also User files data.

![Database object data in data editor](https://resources.jetbrains.com/help/img/idea/2025.3/data_editor_db_object_data_glossary.png)

![Data editor tab in a delimiter-separated values file editor](https://resources.jetbrains.com/help/img/idea/2025.3/data_editor_for_dsv_files_data_intro.png)

For more information about data editor, refer to [Data editor and viewer](data-editor-and-viewer.html).

Database tool window
    

In the Database tool window, you can work with databases and DDL [data sources](managing-data-sources.html#data_sources). You can view and modify data structures in your databases and perform other associated tasks.

The available data sources are shown as a tree of data sources, schemas, tables, and so on.

![Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/db_database_tool_window.png)

For more information about working with database objects in Database tool window, refer to the [Database objects](database-objects.html) section.

For more information about Database tool window, refer to the [Database tool window](database-tool-window.html) topic.

Introspection
    

[Introspection](introspection.html) is a process of loading metadata of a database. When you perform introspection, structural information in the data source is inspected to detect tables, columns, routines, and other database objects with their attributes.

IntelliJ IDEA uses this information to show the objects in Database tool window, display their DDL, suggest them during completion, and for other coding assistance features.

Once you initiate introspection, IntelliJ IDEA displays the introspection progress bars on the right-hand side of the status bar.

![Introspection run process](https://resources.jetbrains.com/help/img/idea/2025.3/introspection_run.png)

By default, only the schemas and databases selected to be shown in the Database tool window are introspected.

For a few databases, three introspection levels are supported to reduce the number of introspected objects. For more information about the levels, refer to the [introspection levels](introspection-levels.html) topic.

Query file
    

Query files are SQL files that are associated with a data source. You can write and execute SQL statements in query files the same way as you do it in terminal. 

![Query file](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_file_overview.png)

For more information about working with query results in query files, refer to [Query results](viewing-query-results.html).

When you create a data source, a query file is created automatically and associated with this data source by default. If necessary, you can create additional query files for this data source. You can also associate a query file with a different data source using the data source dropdown on the toolbar.

By default, query files are stored in the .idea/queries directory . 

Before IntelliJ IDEA version 2025.3, the term used for query file was query console. 

  * For more information about query files, refer to the [Query files](query-files.html) topic.

  * For more information about other types of SQL files in IntelliJ IDEA, refer to [File management](working-with-files.html) topic.



User files
    

User files are the files that are stored on your machine or any other place you have access to. To work with them in IntelliJ IDEA, access the directory that contains them in the Project tool window.

For more information about user files, refer to the [User files](working-with-user-files.html) topic.

For more information about other types of SQL files in IntelliJ IDEA, refer to the [File management](working-with-files.html) topic.

Routines
    

In IntelliJ IDEA, routines combine functions and procedures. You can set Database tool window to display them separately or under a single routines node.

  * Procedures and functions combined under routines node

![Routines display enabled in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/routines_database_tool_window.png)
  * Procedures and functions displayed separately under dedicated nodes

![Routines display disabled in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/routines_database_tool_window_separated.png)



For more information about the Database tool window and its view options, refer to the [Database tool window](database-tool-window.html) topic and [View Options](database-tool-window.html#view_options) chapter.

28 October 2025

[Quick start with database functionality](quick-start-with-database-functionality.html)[Connection to a database](connecting-to-a-database.html)
