[//]: # (Source: https://www.jetbrains.com/help/idea/clouds-aws.html)
[//]: # (Downloaded: 2025-12-17 19:20:06)

# AWS

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




### Step 1. Install a cloud provider plugin

  1. In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar and navigate to Data Source from Cloud Provider | Download Provider Plugin | AWS Cloud Explorer.

![Selecting the AWS cloud provider plugin to download in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/cloud_providers_download_menu_aws.png)
  2. In the Choose Plugins to Install or Enable dialog, make sure that the plugin for your cloud provider is selected. Click OK to confirm.

IntelliJ IDEA downloads the plugin.

  3. Once the cloud provider plugin is downloaded, the provider is available in the same submenu under New | Data Source from Cloud Provider | AWS.




### Step 2. Configure a AWS cloud provider connection

  1. In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar. Navigate to Data Source from Cloud Provider and select AWS.

![Selecting AWS from the cloud provider submenu in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/cloud_providers_select_provider_menu_aws.png)
  2. IntelliJ IDEA opens the Clouds section on the left-hand side of Data Sources and Drivers dialog. Iin this section, enter your cloud provider account connection details on the Configuration tab of the settings area.

     1. From the Regions dropdown, select the AWS Regions of the account that you are connecting to.

     2. From the Authentication type dropdown, select the authentication method you want to use.

        * Default credential providers chain: use the credentials from the default provider chain. For more information about the chain, refer to [Using the Default Credential Provider Chain](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html).

        * Profile from credentials file: select a profile from your credentials file.

        * Explicit access key and secret key: enter your credentials manually.

If you authenticate using a profile from config or credentials file, IntelliJ IDEA enables you to share your MFA or OAuth 2.0 data across all AWS connections. This means that if you select the same profile in AWS S3, AWS EMR, and AWS Glue, you don't have to perform MFA or OAuth 2.0 authentication again.

With the Default credential providers chain or Profile from credentials file option selected, you can click Open Credentials to locate the directory where the credential file is stored. If you use the default location, it's usually ~/.aws/credentials on Linux or macOS, or C:\Users\<USERNAME>\\.aws\credentials on Windows. Or it can be your custom location if you have selected Use custom configs.

     3. You can also set up Extended Connection Settings:

        * HTTP Proxy: select if you want to use [IDE proxy settings](settings-http-proxy.html) or specify custom proxy settings.

![Cloud provider dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_cloud_providers_dialog_aws.png)
  3. Run a test connection by clicking Test connection at the bottom of the connection details area.

  4. Click Apply to save the connection configuration.




### Step 2. Create a data source 

To create a data source for a database stored in the cloud provider, do the following.

  1. In the Clouds section on the left-hand side of the dialog of Data Sources and Drivers dialog, open the Databases tab of the settings area.

  2. On the Databases tab, IntelliJ IDEA displays the list of databases available in the account. Select the databases you want to connect to. To select multiple databases, click them holding `Shift`.

![List of databases available in a cloud account](https://resources.jetbrains.com/help/img/idea/2025.3/db_clouds_available_databases_aws.png)
  3. To create a data source for the selected database, click Create data source.

IntelliJ IDEA saves the cloud provider connection configuration and opens the Data Sources section on the left-hand side of the dialog. The IDE also automatically fills the database connection details in the corresponding fields of the General tab of the settings area.

  4. Type your user credentials.

![Data source settings](https://resources.jetbrains.com/help/img/idea/2025.3/db_clouds_data_source_settings_aws.png)
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




20 November 2025

[Clouds](clouds.html)[Google Cloud](clouds-google-cloud.html)
