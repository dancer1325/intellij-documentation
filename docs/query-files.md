[//]: # (Source: https://www.jetbrains.com/help/idea/query-files.html)
[//]: # (Downloaded: 2025-12-17 19:56:38)

## Overview

Query files are SQL files that are associated with a data source. You can write and execute SQL statements in query files the same way as you do it in terminal. 

![Query file](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_file_overview.png)

For more information about working with query results in query files, refer to [Query results](viewing-query-results.html).

When you create a data source, a query file is created automatically and associated with this data source by default. If necessary, you can create additional query files for this data source. You can also [associate a query file with a different data source](#associate_query_file_with_data_source) using the data source dropdown on the toolbar.

### Location

By default, query files are stored in the .idea/queries directory . 

Syntax
    

%HOMEPATH%\<product>Projects\<project_name>\\.idea\dataSources\queries

Example
    

C:\Users\JohnS\IntelliJIdeaProjects\my_project\\.idea\dataSources\queries

Syntax
    

~/<product>Projects/<project_name>/.idea/dataSources/queries

Example
    

~/IntelliJIdeaProjects/my_project/.idea/dataSources/queries

Syntax
    

~/<product>Projects/<project_name>/.idea/dataSources/queries

Example
    

~/IntelliJIdeaProjects/my_project/.idea/dataSources/queries

In the IDE, you can find the directory in the Project tool window `Alt+1`.

Before IntelliJ IDEA version 2025.3, the term used for query file was query console. The consoles were located in the internal Database Consoles directory.

Starting from IntelliJ IDEA version 2025.3, query consoles are migrated to query files. Old consoles are kept in the same directory as preciously to guarantee safety and backward compatibility. To access this folder, open the Project tool window `Alt+1` and navigate to Scratches and Consoles | Database Consoles. On your machine, the query file files are stored in the consoles subdirectory of the [IDE configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

### Change the query files directory

  1. Press `Ctrl+Alt+S` to open settings and then select Tools | Database | Query Files. 

  2. In the Query files directory field, specify the directory.

  3. Apply the changes and close the dialog.




### Code editor

The code editor is where you compose your SQL statements using the [resolve modes](run-a-query.html#resolve_modes) and coding assistance features, and execute them against the associated data source.

Find the code editor toolbar controls in [Code editor controls](#reference). Read more about the editor in [Editor basics](using-code-editor.html).

### SQL statement execution

When you execute a statement, the Services tool window opens. The Services tool window displays available connection sessions, Output and Result tabs. For more information about the tool window, refer to the[Services tool window](services-tool-window.html) topic. 

  * If the executed statement retrieves data (for example, `SELECT`), results are displayed in the Result tab that has a title of a qualified table name. For more information about creating custom titles for result tabs, refer to [Use custom titles for tabs with results](viewing-query-results.html#use-custom-titles-for-tabs-with-results).

  * If the executed statement does not retrieve data, results are displayed in the Output tab.

![Query file with an active Result tab of Services tool window](https://resources.jetbrains.com/help/img/idea/2025.3/db_ui_query_file_result_tab.png)
    1. [Query file tab toolbar](#toolbar_controls).

    2.     3. Services tool window.

    4. [Output](services-tool-window.html#db_output_tab) and [Result](services-tool-window.html#db_result_tab) tabs. Result tab is active.

    5. [Result tab toolbar](services-tool-window.html#db_result_tab_toolbar). 

![Query file with an active Output tab of Services tool window](https://resources.jetbrains.com/help/img/idea/2025.3/db_ui_query_file_output_tab.png)
    1. [Query file tab toolbar](#toolbar_controls).

    2.     3. Services tool window.

    4. [Output](services-tool-window.html#db_output_tab) and [Result](services-tool-window.html#db_result_tab) tabs. Output tab is active.

    5. [of the Output tab](services-tool-window.html#db_output_tab_right_toolbar). 



