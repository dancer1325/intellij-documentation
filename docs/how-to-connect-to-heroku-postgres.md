[//]: # (Source: https://www.jetbrains.com/help/idea/how-to-connect-to-heroku-postgres.html)
[//]: # (Downloaded: 2025-12-17 19:28:47)

# Create a PostgreSQL data source for Heroku Postgres without SSL validation

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




If you want to connect to Heroku Postgres, create a data source connection that corresponds to the data source vendor. In this case, you plan to work with PostgreSQL, so you need to create a connection to PostgreSQL. IntelliJ IDEA already include the necessary JDBC driver.

Heroku Postgres requires you to use SSL for the connection. But for establishing a successful SSL connection, you need a certificate that you have to upload to your Heroku application. SSL certificates are specific for each Heroku application. To configure these certificates, see the article about [Heroku SSL](https://devcenter.heroku.com/articles/ssl).

If you do not plan to add the certificate in the keystore, you can bypass the server validation with the `NonValidatingFactory` option and establish an encrypted connection.

  1. In your Heroku account, create an application with the Heroku Postgres add-on.

  2. In the settings of the Heroku Postgres add-on, get the database credentials.

To connect to a database, create a data source that will store your connection details.

  3. Select the data source you want to create. You can do this using one of the following ways:

     * In the main menu, go to File | New | Data Source and select PostgreSQL.

     * In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar. Navigate to Data Source and select PostgreSQL.

![Create a new data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source.png)
  4. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. For a direct download link, refer to the [JetBrains JDBC drivers](https://www.jetbrains.com/datagrip/jdbc-drivers/) page. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)

Location for the downloaded JDBC drivers is the [IntelliJ IDEA configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

You can also use your drivers for the database instead of the provided ones. For more information about connecting to a database with your driver, refer to [Add a user driver to an existing connection](jdbc-drivers.html#configure_a_jdbc_driver_for_an_existing_data_source).

If there is no Download missing driver files link, then you already have the required drivers.

  5. Specify the database connection details. Alternatively, paste the JDBC URL in the URL field.

     * In Host, Database, User, Password, and Port fields, specify connection details that you received for the Heroku Postgres add-on.

For the reference information about on the General and other tabs of Data Sources and Drivers dialog ( `Shift+Enter`) , see .

  6. In the SSH/SSL tab of Data Sources and Drivers dialog, select the Use SSL checkbox.

  7. In the Advanced tab of Data Sources and Drivers dialog, change the value of the following property:

     * `sslfactory:org.postgresql.ssl.NonValidatingFactory`: to allow SSL connections without validating the server certificate.

  8. Ensure that the database connection can be established using the provided details. To do this, click the Test Connection link at the bottom of the connection details section.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)

If you encounter any connection issues, refer to the [Cannot connect to a database](connectivity-problems.html) page.

  9. (Optional) By default, only the default database is introspected and available to work with. If you also want to work with other databases, in the Schemas tab, select them for the introspection.

![Schemas tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_schemas_tab.png)
  10. Click OK to create the data source.

  11. Find your new data source in the Database tool window.

     * For more information about the Database tool window, see the corresponding [reference topic](database-tool-window.html).

To see more databases under your new data source node, click the N of M button and select the ones you need. IntelliJ IDEA will introspect and show them.

![Select databases and schemas to introspect and display in the Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/connection_flow_show_databases_and_schemas.png)
     * For more information about working with database objects in IntelliJ IDEA, refer to [Database objects](database-objects.html).

     * To write and run queries, open the default [query file](query-files.html) by clicking the data source and pressing `F4`.

     * To view and edit data of a database object, open [Data editor and viewer](data-editor-and-viewer.html) by double-clicking the object.


![Integration with Heroku Postgres](https://resources.jetbrains.com/help/img/idea/2025.3/db_heroku_postgres_integration.png)

For more information about the Heroku Postgres provision, refer to the official documentation at [Heroku Dev Center](https://devcenter.heroku.com).

28 October 2025

[PostgreSQL](postgresql.html)[Redis](redis.html)
