[//]: # (Source: https://www.jetbrains.com/help/idea/cannot-connect-to-mysql-5-1.html)
[//]: # (Downloaded: 2025-12-17 19:19:39)

# Cannot connect to MySQL 5.1

To connect to a database, create a data source that will store your connection details.

  1. Select the data source you want to create. You can do this using one of the following ways:

     * In the main menu, go to File | New | Data Source and select MySQL.

     * In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar. Navigate to Data Source and select MySQL.

![Create a new data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source.png)
  2. Click the Driver link and select MySQL for 5.1.

  3. To download JDBC drivers for MySQL 5.1, click the Download link at the bottom of the dialog.

Specify the database connection details. Alternatively, paste the JDBC URL in the URL field.

To delete a password, right-click the Password field and select Set Empty.

  4. Specify the database connection details. Alternatively, paste the JDBC URL in the URL field.

To delete a password, right-click the Password field and select Set Empty.

![General tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_general_tab.png)

For the reference information about connection settings (for example, Host, Port, and so on) on the General and other tabs of Data Sources and Drivers dialog ( `Shift+Enter`) , see [Data Sources](data-sources-and-drivers-dialog.html#db).

  5. Ensure that the database connection can be established using the provided details. To do this, click the Test Connection link at the bottom of the connection details section.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)

If you encounter any connection issues, refer to the [Cannot connect to a database](connectivity-problems.html) page.

  6. (Optional) By default, only the default schema is introspected and available to work with. If you also want to work with other schemas, in the Schemas tab, select them for the introspection.

![Schemas tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_schemas_tab.png)
  7. Click OK to create the data source.

  8. Find your new data source in the Database tool window.

     * For more information about the Database tool window, see the corresponding [reference topic](database-tool-window.html).

To see more schemas under your new data source node, click the N of M button and select the ones you need. IntelliJ IDEA will introspect and show them.

![Select databases and schemas to introspect and display in the Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/connection_flow_show_databases_and_schemas.png)
     * For more information about working with database objects in IntelliJ IDEA, refer to [Database objects](database-objects.html).

     * To write and run queries, open the default [query file](query-files.html) by clicking the data source and pressing `F4`.

     * To view and edit data of a database object, open [Data editor and viewer](data-editor-and-viewer.html) by double-clicking the object.


![Connect to MySQL 5.1](https://resources.jetbrains.com/help/img/idea/2025.3/db_connect_to_mysql_51.png)

### Cannot connect to MySQL 5.* in the cloud with SSL

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. Click the Driver link and select Go to Driver.

  3. In the Driver Files pane, click the ver. *.*.*.* link and select 5.1.40.

  4. Click the created MySQL data source entry.

Specify the database connection details. Alternatively, paste the JDBC URL in the URL field.

To delete a password, right-click the Password field and select Set Empty.

  5. Specify the database connection details. Alternatively, paste the JDBC URL in the URL field.

To delete a password, right-click the Password field and select Set Empty.

![General tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_general_tab.png)

For the reference information about connection settings (for example, Host, Port, and so on) on the General and other tabs of Data Sources and Drivers dialog ( `Shift+Enter`) , see [Data Sources](data-sources-and-drivers-dialog.html#db).

  6. Ensure that the database connection can be established using the provided details. To do this, click the Test Connection link at the bottom of the connection details section.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)

If you encounter any connection issues, refer to the [Cannot connect to a database](connectivity-problems.html) page.

  7. (Optional) By default, only the default schema is introspected and available to work with. If you also want to work with other schemas, in the Schemas tab, select them for the introspection.

![Schemas tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_schemas_tab.png)
  8. Click OK to create the data source.

  9. Find your new data source in the Database tool window.

     * For more information about the Database tool window, see the corresponding [reference topic](database-tool-window.html).

To see more schemas under your new data source node, click the N of M button and select the ones you need. IntelliJ IDEA will introspect and show them.

![Select databases and schemas to introspect and display in the Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/connection_flow_show_databases_and_schemas.png)
     * For more information about working with database objects in IntelliJ IDEA, refer to [Database objects](database-objects.html).

     * To write and run queries, open the default [query file](query-files.html) by clicking the data source and pressing `F4`.

     * To view and edit data of a database object, open [Data editor and viewer](data-editor-and-viewer.html) by double-clicking the object.




28 October 2025

[Create a MySQL data source using unix sockets](how-to-connect-to-mysql-with-unix-sockets.html)[Oracle](oracle.html)
