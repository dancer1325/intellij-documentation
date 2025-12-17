[//]: # (Source: https://www.jetbrains.com/help/idea/modifying-source-code-of-database-objects.html)
[//]: # (Downloaded: 2025-12-17 19:32:31)

## Updating source code

IntelliJ IDEA retrieves the information about a database during the introspection process. This information is used to show the objects in the Database tool window, display their DDL, suggest them during completion, and in other features for coding assistance.

You can update the source code of database objects directly by editing their DDL and submitting your changes. The IDE will generate a migration script and execute it in the database.

The Database Changes tool window displays a summary of all your changes.

### Load source code for a data source

IntelliJ IDEA retrieves the source code for a data source during the introspection. You can manage this process in the data source properties.

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. Select one or more data sources for which you want to download source code.

  3. Right-click the selection and navigate to Load Sources. You can select between the following options:

     * None: do not download source code.

     * Except System Schemas: download source code for all the objects except for system schemas.

     * All Schemas: download all the available source code.

![Load source code for a data source](https://resources.jetbrains.com/help/img/idea/2025.3/db_load_source_code_for_data_source.png)



### Edit source code of an object

You can update the source code of database objects by directly editing their DDL `CREATE` scripts and submitting your changes in the editor. The IDE will generate a migration script with your changes, prompt you to verify it, and then execute it in the database.

  1. Right-click an object and select Navigation | Go to DDL. Alternatively, press `Ctrl+B`. 

The object references in the generated script are not qualified (for example, `<view_name>` instead of `<schema_name>.<view_name>`). You can view this script, edit it, and submit your changes to the database. 

For a runnable DDL script that includes `CREATE OR REPLACE`, qualified references, and so on, use the [SQL Generator](export-data.html#generate-ddl-definitions-for-dat).

  2. Make changes to source code.

  3. (Optional) In the Database Changes tool window (View | Tool Windows | Database Changes), double-click the modified object to open the Diff Viewer and verify your changes.

  4. Click the Submit button (![the Submit button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg)).

When you click the Submit button (![the Submit button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg)) in the Database Changes tool window, you see the Migration dialog. The Migration dialog displays a migration script for the object.

  5. In the Object Migration dialog, verify that the migration script is correct and click OK.

A migration script is code that changes the entire database or a part of it. You can use migration scripts to add or remove a column, upgrade the database version, or change column properties.

IntelliJ IDEA can automatically generate a migration script, but you have to check it before running.




### See all the changes in source code

  * Select View | Tool Windows | Database Changes from the main menu.

The Database Changes tool window becomes available only after you change the source code of a database object.

![the Database Changes tool window](https://resources.jetbrains.com/help/img/idea/2025.3/db_database_changes_tool_window.png)



### See the difference between modified and stored versions

  * When you edit the source code of any object, IntelliJ IDEA tracks changes and highlights them in the gutter. For example, add a comment line to a routine or a trigger function. The added line becomes highlighted. If you click the highlighted line in the gutter, a small toolbar is displayed with the Show Diff for Lines button. You can click the Show Diff for Lines button (![the Show Diff icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg)) to see the difference between the code that you added and the one from source code.

![IDE highlights changes in source code](https://resources.jetbrains.com/help/img/idea/2025.3/db_diff_via_code_editor.png)
  * In the Database Changes tool window (View | Tool Windows | Database Changes), double-click the modified object to open the Diff Viewer and verify your changes.

![the Database Changes tool window](https://resources.jetbrains.com/help/img/idea/2025.3/db_diff_via_database_changes.png)


