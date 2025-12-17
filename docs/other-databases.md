[//]: # (Source: https://www.jetbrains.com/help/idea/other-databases.html)
[//]: # (Downloaded: 2025-12-17 19:33:37)

## Creating data sources from drivers with basic support

There are two ways to create data sources from drivers with basic support.

  * Using the Other submenu

  * Using user driver files




### Using the Other submenu

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. In the Data Sources and Drivers dialog, you can use Data Sources and Drivers tabs to create a data source.

     * Data Sources: click the Add icon (![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and navigate to Other. In this submenu, select the driver that you want to use for the data source creation.

     * Drivers: click the Drivers tab and select the necessary driver. In the settings of this driver, click Create Data Source.

  3. Specify the database connection details. Alternatively, paste the JDBC URL in the URL field.

To delete a password, right-click the Password field and select Set Empty.

![General tab of the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_general_tab.png)

For the reference information about connection settings (for example, Host, Port, and so on) on the General and other tabs of Data Sources and Drivers dialog ( `Shift+Enter`) , see [Data Sources](data-sources-and-drivers-dialog.html#db).

  4. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. For a direct download link, refer to the [JetBrains JDBC drivers](https://www.jetbrains.com/datagrip/jdbc-drivers/) page. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)

Location for the downloaded JDBC drivers is the [IntelliJ IDEA configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

You can also use your drivers for the database instead of the provided ones. For more information about connecting to a database with your driver, refer to [Add a user driver to an existing connection](jdbc-drivers.html#configure_a_jdbc_driver_for_an_existing_data_source).

If there is no Download missing driver files link, then you already have the required drivers.

  5. Ensure that the database connection can be established using the provided details. To do this, click the Test Connection link at the bottom of the connection details section.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)

If you encounter any connection issues, refer to the [Cannot connect to a database](connectivity-problems.html) page.

  6. Click OK to create the data source.


![Drivers that have basic support](https://resources.jetbrains.com/help/img/idea/2025.3/db_drivers_with_basic_support.png)

### Using user driver files

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. In the Data Sources and Drivers dialog, ensure that you are on the Drivers tab.

  3. In the Data Sources and Drivers dialog, click the Add icon (![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)).

  4. In the Name field, type the name of the driver.

  5. In the Driver Files pane, click the Add icon (![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and select Custom JARs.

  6. Navigate to the JAR file of the JDBC driver, select it, and click OK.

  7. In the Class field, specify the value that you want to use for the driver.

  8. Click Apply.

  9. To create a data source from the driver's dialog, click Create Data Source. 



