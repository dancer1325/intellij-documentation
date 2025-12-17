[//]: # (Source: https://www.jetbrains.com/help/idea/jdbc-drivers.html)
[//]: # (Downloaded: 2025-12-17 19:30:24)

# JDBC drivers

JDBC (Java Database Connectivity) driver enables the IDE to connect to and query a database.

IntelliJ IDEA does not include bundled drivers to have a smaller size of the installation package and to keep driver versions up to date for each IDE version.

You can download JDBC drivers within the IDE and manually:

  * Upon [creating a new data source](managing-data-sources.html#create_a_data_source) for your database connection in the Data Sources and Drivers dialog ( `Shift+Enter`) , IntelliJ IDEA provides a link for you to download the missing driver.

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)
  * For direct download links, refer to the [JetBrains JDBC drivers](https://www.jetbrains.com/datagrip/jdbc-drivers/) page.




Location for the downloaded JDBC drivers is the [IntelliJ IDEA configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

If you need to download the driver from a Maven mirror or your own repository, IntelliJ IDEA will use the one configured in the $USER_HOME$/.m2/settings.xml file. For more information about the file, refer to the [official documentation](https://maven.apache.org/settings.html).

You can also [specify your drivers](#configure_a_jdbc_driver_for_an_existing_data_source) for the data source instead of the provided ones. Custom JDBC drivers can be sourced from official database vendor websites, open source repositories, third-party vendors, developer communities and forums, and so on.

### Change the driver version

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. In the Data Sources and Drivers dialog, click the Drivers tab, and select a driver entry that you want to modify.

  3. Click the Driver link in data source settings.

Some data sources have a list with drivers for different versions (for example, MySQL). In these cases, select Go to driver from the list.

  4. In the Driver files pane, click the version number and select the driver version that you need.




### Configure a JDBC driver for an existing data source

You can add libraries to the existing driver or replace the driver completely.

To work properly, some JDBC drivers require a path to library files along with the driver. For more information about library paths, refer to [Library paths for user drivers](other-databases.html#library-paths-for-user-drivers).

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. Click the Driver link in data source settings and select Go to Driver.

  3. Click the provided driver entry, and click Remove (![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)).

To revert changes, click the Roll back Changes icon (![the Roll back Changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.diff.revert.svg)) that is in the lower-right part of the window.

  4. In the Driver Files pane, click the Add icon (![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and select Custom JARs.

  5. In the file browser, navigate to the JAR file of the JDBC driver, select it, and click OK.

  6. In the Class field, specify the value that you want to use for the driver.

Driver class is a driver-specific main class for a JDBC driver. For the proper driver class for the JDBC driver you use, refer to the driver's documentation.

If the field is empty, or a predefined value is different from the one your driver requires, specify the required value manually.

  7. If your custom driver requires an additional property, go to the Advanced tab in the dialog. In the properties pane, enter the additional property's name and value in the last row of Name and Value columns, where <user defined> and <value> are shown.

  8. Click Apply.




For more information about about JDBC driver settings, refer to [the dialog reference topic](data-sources-and-drivers-dialog.html#driver).

28 October 2025

[Connect to a database with SSH](connect-to-a-database-with-ssh.html)[Data Sources and Drivers dialog](data-sources-and-drivers-dialog.html)
