[//]: # (Source: https://www.jetbrains.com/help/idea/run-sql-files.html)
[//]: # (Downloaded: 2025-12-17 19:59:10)

## Run an SQL file

  1. Open the Run/Debug Configuration dialog in one of the following ways:

     * Select Run | Edit Configurations from the main menu.

     * With the [Navigation bar](guided-tour-around-the-user-interface.html#navigation-bar) visible (View | Appearance | Navigation Bar), choose Edit Configurations from the run/debug configuration selector. 

     * Press `Alt+Shift+F10` and then press `0`.

  2. In the Run/Debug Configurations dialog, you can either create a new run configuration or edit an existing one.

     * To create a new run configuration, click the Add New Configuration icon (![the Add New Configuration icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and select Database Script.

     * To edit an existing run configuration, expand the Database Script node and select the run configuration that you want to edit from the list.

  3. The fields that appear in the right-hand pane display the settings for the selected configuration type.

     * Target data source / schema: databases or schemas against which you want to run your database scripts. This setting is dialect-dependent.

If you select a data source as a target, IntelliJ IDEA displays a schema in which the script will be run. It is the default schema.

     * Script files: SQL files that you want to run. To add files, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and navigate to files that you want to run. If a script contains schema switching, you will see a warning (![Warning](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.warning.svg)).

  4. You can either run the configuration right away or save the configuration to run it later.

     * To save the run configuration for later, click OK.

     * To run the configuration right away, click Run.


![Run files by using run/debug configurations](https://resources.jetbrains.com/help/img/idea/2025.3/db_run_debug_configurations_script_files.png)

  1. In the Project tool window, right-click the SQL file that you want to run, and select Run '<file_name>'. Alternatively, press `Alt+Shift+R`.

![Run SQL files from the Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/run_sql_files_from_project_tool_window.png)
  2. Select the settings for your run configuration.

     * Target data source / schema: databases or schemas against which you want to run your database scripts. This setting is dialect-dependent.

If you select a data source as a target, IntelliJ IDEA displays a schema in which the script will be run. It is the default schema.

     * Script files: SQL files that you want to run. To add files, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and navigate to files that you want to run. If a script contains schema switching, you will see a warning (![Warning](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.warning.svg)).

![Edit Configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_run_configuration_select_target.png)
  3. Click Run.




  1. In the Database tool window, right-click a data source, or a schema and select SQL Scripts | Run SQL Script. 

![Run an SQL file from the Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/run_sql_file_from_database_tool_window.png)
  2. In the file browser window that opens, navigate to the SQL file that you want to run.

  3. Click Open.

You can view the output in the Run tool window. For more information about tool window controls, refer to [Run tool window](run-tool-window.html). 




  1. Open the Project tool window `Alt+1`, navigate to the SQL file, and select it.

  2. Drag the SQL file to Database tool window to the data source, database, or schema that you want to run it against.

  3. Select the settings for your run configuration.

     * Target data source / schema: databases or schemas against which you want to run your database scripts. This setting is dialect-dependent.

If you select a data source as a target, IntelliJ IDEA displays a schema in which the script will be run. It is the default schema.

     * Script files: SQL files that you want to run. To add files, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and navigate to files that you want to run. If a script contains schema switching, you will see a warning (![Warning](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.warning.svg)).

![Edit Configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_run_configuration_select_target.png)
  4. Click Run.




You can run single files using a dedicated option on the toolbar. The run and debug buttons are active and allow you to instantly run the currently opened file.

  1. In the editor, open the file that you want to run.

  2. Click ![Run](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) next to the Current File option on the toolbar. 

  3. Select the settings for your run configuration.

     * Target data source / schema: databases or schemas against which you want to run your database scripts. This setting is dialect-dependent.

If you select a data source as a target, IntelliJ IDEA displays a schema in which the script will be run. It is the default schema.

     * Script files: SQL files that you want to run. To add files, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and navigate to files that you want to run. If a script contains schema switching, you will see a warning (![Warning](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.warning.svg)).

![Edit Configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_run_configuration_select_target.png)
  4. Click Run.




You can access the other run modes by expanding the list. From the widget that opens, you can debug the code, run it with coverage, profile it, or open the run configuration to specify more options.
