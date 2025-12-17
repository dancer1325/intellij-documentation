[//]: # (Source: https://www.jetbrains.com/help/idea/connect-to-bigquery.html)
[//]: # (Downloaded: 2025-12-17 19:22:13)

## Google user account

When you use authorization with the Google user account, you need to receive the authorization code in a web browser.

### Connect to Google BigQuery

To connect to a database, create a data source that will store your connection details.

  1. Select the data source you want to create. You can do this using one of the following ways:

     * In the main menu, go to File | New | Data Source and select Google BigQuery.

     * In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar. Navigate to Data Source and select Google BigQuery.

![Create a new data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source.png)
  2. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. For a direct download link, refer to the [JetBrains JDBC drivers](https://www.jetbrains.com/datagrip/jdbc-drivers/) page. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)

Location for the downloaded JDBC drivers is the [IntelliJ IDEA configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

You can also use your drivers for the database instead of the provided ones. For more information about connecting to a database with your driver, refer to [Add a user driver to an existing connection](jdbc-drivers.html#configure_a_jdbc_driver_for_an_existing_data_source).

If there is no Download missing driver files link, then you already have the required drivers.

  3. From the Authentication list, select Google User Account.

  4. In the Project ID field, type the project ID.

Usually, it is a part of the service account email that goes after the at sign (`@`). For example, `bigqueryproject-322409`. For the project ID's format, refer to the [official instructions on creating a service account](https://cloud.google.com/iam/docs/service-accounts-create).

  5. From the Authorization Code Required dialog, cut the URL, paste it into the address bar of your web browser, and press `Enter` to follow the URL.

  6. Authorize access to your Google BigQuery application in your Google account.

  7. Copy the authorization code received from Google, paste it in the Authorization Code Required dialog, and click OK.

  8. Ensure that the database connection can be established using the provided details. To do this, click the Test Connection link at the bottom of the connection details section.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)

If you encounter any connection issues, refer to the [Cannot connect to a database](connectivity-problems.html) page.

  9. (Optional) By default, only the default project and dataset are introspected and available to work with. If you also want to work with other projects and datasets, in the Schemas tab, select them for the introspection.

![Schemas tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_schemas_tab.png)
  10. Click OK to create the data source.

  11. Find your new data source in the Database tool window.

     * For more information about the Database tool window, see the corresponding [reference topic](database-tool-window.html).

To see more projects and datasets under your new data source node, click the N of M button and select the ones you need. IntelliJ IDEA will introspect and show them.

![Select databases and schemas to introspect and display in the Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/connection_flow_show_databases_and_schemas.png)
     * For more information about working with database objects in IntelliJ IDEA, refer to [Database objects](database-objects.html).

     * To write and run queries, open the default [query file](query-files.html) by clicking the data source and pressing `F4`.

     * To view and edit data of a database object, open [Data editor and viewer](data-editor-and-viewer.html) by double-clicking the object.



