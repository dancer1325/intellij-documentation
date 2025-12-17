[//]: # (Source: https://www.jetbrains.com/help/idea/how-to-connect-to-cassandra-with-ssl.html)
[//]: # (Downloaded: 2025-12-17 19:28:46)

## Step 1. Create a Apache Cassandra data source

To connect to a database, create a data source that will store your connection details.

  1. Select the data source you want to create. You can do this using one of the following ways:

     * In the main menu, go to File | New | Data Source and select Apache Cassandra.

     * In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar. Navigate to Data Source and select Apache Cassandra.

![Create a new data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source.png)
  2. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. For a direct download link, refer to the [JetBrains JDBC drivers](https://www.jetbrains.com/datagrip/jdbc-drivers/) page. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)

Location for the downloaded JDBC drivers is the [IntelliJ IDEA configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

You can also use your drivers for the database instead of the provided ones. For more information about connecting to a database with your driver, refer to [Add a user driver to an existing connection](jdbc-drivers.html#configure_a_jdbc_driver_for_an_existing_data_source).

If there is no Download missing driver files link, then you already have the required drivers.

  3. In Host, Keyspace, User, Password, and Port fields, specify connection details.



