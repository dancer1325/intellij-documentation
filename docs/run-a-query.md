[//]: # (Source: https://www.jetbrains.com/help/idea/run-a-query.html)
[//]: # (Downloaded: 2025-12-17 19:57:51)

## Run statements and procedures

### Run statements in a query file

You can relate to a query file as to a terminal where you type and run your code.

  1. In the Database tool window, click the data source.

  2. Press `F4` to open a query file. For more information about working with query files, refer to [Work with query files](query-files.html#work_with_query_files).

  3. Type or paste the statement that you want to execute.

  4. Click ![the Execute button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) Execute on the toolbar. Alternatively, press `Ctrl+Enter`.

If you have several statements, select whether you want to execute all statements or a single statement. The suggestion list always contains an item for running all the statements. 

![Run a query](https://resources.jetbrains.com/help/img/idea/2025.3/db_run_query.png)



### Run statements from an open file

In IntelliJ IDEA, you can open and run a file. The limitation for the file size is 20 MB. When you open a file that is larger than 20 MB, you see only first 2.5 MB of the file. The file should be associated with the SQL file type. For more information about file type associations, refer to the [File type associations](creating-and-registering-file-types.html#configure-associations-between-filename-patterns-and-file-types) topic. 

  1. Open the Project tool window (View | Tool Windows | Project) and double-click an SQL file.

For more information about attaching directories and files in IntelliJ IDEA, refer to [User files](working-with-user-files.html).

  2. Click the statement that you want to execute.

Also, you can select (highlight) the fragment of code that you want to execute. It can be a subquery or a group of statements. IntelliJ IDEA executes only the selection.

  3. Click the Execute button (![the Execute button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg)) on the toolbar. Alternatively, press `Ctrl+Enter`.

To customize query execution settings, click the Customize link. Alternatively, open settings by pressing `Ctrl+Alt+S` and navigate to Tools | Database | Query Execution. .

  4. (Optional) If the SQL file is not attached to a data source, select the data source that you want to attach it to in the <data source> list.

For more information about attaching SQL files to data sources, refer to [Data source attachment](run-sql-files.html#data_source_attachment).

  5. In the Statements window, press `Enter` to run the selected statement. You can switch between other entries to run another set of statements. Statements that you are going to execute are highlighted in a query editor.

In the Statements window, you can click Customize to define whether you want to see the chooser or always run the statement under the caret.

For another example of running script files, refer to [the following video at youtube.com](https://www.youtube.com/watch?v=U5SOD-eeK50&t=1913s).




### Run stored procedures

A stored procedure is a set of SQL statements with an assigned name. You can execute stored procedures in PostgreSQL, Microsoft SQL Server, Oracle, and MySQL.

  1. Right-click a stored function that you want to execute and select Run Function.

  2. In the Execute Routine window, type all the necessary parameter values, and click OK.

If necessary, select the Run from checkbox and select the file or console to run the stored function from.

[![Run stored procedures](https://resources.jetbrains.com/help/img/idea/2025.3/run_stored_functions.png)](https://resources.jetbrains.com/help/img/idea/2025.3/run_stored_functions.png)



### Run SELECT statements and save results into files

  1. (Optional) If the file is not connected to a data source, select a data source from the list of data sources on the toolbar. Then select the connection session from the Sessions list.

For more information about connection sessions, refer to [Sessions](managing-connection-sessions.html).

  2. Right-click a `SELECT` statement.

  3. Select Execute to File and select the output format.

  4. In the Export Data dialog, specify the extractor that you want to use and other settings.

For more information about the Export Data dialog, refer to the [Export data](export-data.html#export-data-from-the-database-tool-window) topic.


![Save the result of a SELECT statement into a file](https://resources.jetbrains.com/help/img/idea/2025.3/db_execute_to_file.png)
