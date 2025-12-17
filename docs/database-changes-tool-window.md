[//]: # (Source: https://www.jetbrains.com/help/idea/database-changes-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:24:01)

# Database Changes tool window

IntelliJ IDEA tracks changes you make to the source code of any database object, provided its source code is stored in a database. For example, such objects are views, stored procedures, triggers, and so on. Tables do not have stored source code.

If there are various changes made to the source code of many objects, you can see all of them in the Database Changes tool window.

The Database Changes tool window becomes available only after you change the source code of a database object.

![the Database Changes tool window](https://resources.jetbrains.com/help/img/idea/2025.3/db_diff_via_database_changes.png)

Icon| Action and shortcut| Description  
---|---|---  
![the Submit button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg)| Submit`Ctrl+K`| Submit local changes to the database server. For more information about submitting and reverting changes, refer to [Submit changes to a database](submitting-and-reverting-changes.html).  
![the Roll back icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.revert.svg)| Roll back`Ctrl+Alt+Z`| (For the Manual transaction mode.) Roll back changes.   
![the Show Diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg)| Show Diff`Ctrl+D`| Compare and see the difference between the code that you edited and the one from source code.  
![the Group by icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg)| Group by| Group objects according to their type. For example, routines, rules, or views.  
![the Expand All icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.expandAll.svg)| Expand All`Ctrl+NumPad +`| Expand all nodes in all trees.  
![the Collapse All icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.collapseAll.svg)| Collapse All`Ctrl+NumPad -`| Collapse all nodes in all trees.  
  
20 June 2025

[Modify source code of database objects](modifying-source-code-of-database-objects.html)[Working with DDL definitions](working-with-ddl-definitions.html)
