[//]: # (Source: https://www.jetbrains.com/help/idea/create-snowflake-data-source-with-key-pair-authentication.html)
[//]: # (Downloaded: 2025-12-17 19:23:07)

# Create a Snowflake data source with key pair authentication

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




### Official documentation

  * For full information about Snowflake, refer to [the official documentation](https://docs.snowflake.net/manuals/user-guide.html).

  * [Key-pair authentication and key-pair rotation at docs.snowflake.com](https://docs.snowflake.com/en/user-guide/key-pair-auth)




Before connecting to a Snowflake database with key pair authentication, make sure to [generate your key files](https://docs.snowflake.com/en/user-guide/key-pair-auth#configuring-key-pair-authentication) and provide your public key file to your system administrator first.

Once the key files are ready, you need to create a Snowflake data source in IntelliJ IDEA and configure it to use it with key pair authentication. 

### Create a Snowflake data source to use with key pair authenticatoin

  1. In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar and navigate to Data Source | Snowflake. 

![Select the Snowflake data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source_snowflake.png)
  2. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. For a direct download link, refer to the [JetBrains JDBC drivers](https://www.jetbrains.com/datagrip/jdbc-drivers/) page. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)
  3. Specify the database connection details. 

     1. In the Host field, type the URL to connect to your Snowflake account with. For example, `myorg-myconnection.snowflakecomputing.com`.

     2. From the Authentication dropdown, select Authenticator.

     3. In the Authenticator field, type `snowflake_jwt`.

     4. In the User field, type your Snowflake username.

     5. Leave the Password field empty. 

You can set the Password field empty by right-clicking it and selecting Set Empty.

![the Set Empty context menu action](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_password_set_empty.png)
     6. In the Database field, type the database name to which you want to connect. 

     7. In the Schema field, type the schema name to which you want to connect.

     8. In the Warehouse field, type the name of a compute resources cluster in Snowflake that you want to use. 

  4. On the SSH/SSL tab of Data Sources and Drivers dialog, select the Use SSL checkbox.

  5. In the Client key file field, click ![the Browse icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.browse.svg) Browse, navigate to your .p8 private key file, select it and click Open.

IntelliJ IDEA supports using private key files in WSL on Windows. To do this, specify the WSL path for your private key file. For example, `\\wsl$\Ubuntu\home\myuser\snowflake\rsa_key.p8`.

  6. For an encrypted private key file, type the passphrase you used when creating it in the Client key password field.

  7. Click the Test Connection link at the bottom of the connection details area to initiate a test connection to your database.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)
  8. Click OK to save your new data source.




Alternatively to specifying connection details in dedicated fields, type your JDBC URL in the URL field of General tab. The general URL to use is as follows:

  * Format:

`jdbc:snowflake://<organization_name>-<connection_name>.snowflakecomputing.com/?warehouse=<warehouse_name>&db=<database_name>&schema=<schema_name>&user=<snowflake_username>&private_key_file=<path_to_key_file>`

  * Example:

`jdbc:snowflake://myorg-myconnection.snowflakecomputing.com/?warehouse=AUTH_WH&db=TESTDB&schema=MYSCHEMA&user=MYUSERNAME&private_key_file=/home/myuser/snowflake/rsa_key.p8`

`jdbc:snowflake://myorg-myconnection.snowflakecomputing.com/?warehouse=AUTH_WH&db=TESTDB&schema=MYSCHEMA&user=MYUSERNAME&private_key_file=С:/Users/myuser/snowflake/rsa_key.p8`

`jdbc:snowflake://myorg-myconnection.snowflakecomputing.com/?warehouse=AUTH_WH&db=TESTDB&schema=MYSCHEMA&user=MYUSERNAME&private_key_file=//wsl$/Ubuntu/home/myuser/snowflake/rsa_key.p8`

`jdbc:snowflake://myorg-myconnection.snowflakecomputing.com/?warehouse=AUTH_WH&db=TESTDB&schema=MYSCHEMA&user=MYUSERNAME&private_key_file=/Users/myuser/snowflake/rsa_key.p8`




In this case, make sure to enable SSL connection on the SSH/SSL tab of the dialog. Also, provide your passphrase in the corresponding field, if required.

  * General tab

![Database connection details](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_details_snowflake_key_pair_general.png)
  * SSH/SSL tab

![Database connection details](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_details_snowflake_key_pair_ssh_ssl.png)



28 October 2025

[Snowflake](snowflake.html)[Create Snowflake data sources with Okta SSO and Duo MFA](create-snowflake-data-sources-with-okta-and-duo.html)
