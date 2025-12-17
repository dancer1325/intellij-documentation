[//]: # (Source: https://www.jetbrains.com/help/idea/connect-to-a-database-with-ssh.html)
[//]: # (Downloaded: 2025-12-17 19:22:12)

## Cloud database

Let us consider the following example. MySQL database is running remotely in a cloud, the connection has to be established through a jump host. You need to authenticate using your encrypted private key file. To create a data source and run a test connection to your database, do the following:

  1. In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar and navigate to Data Source | MySQL. 

  2. Click the SSH/SSL tab and select the Use SSH tunnel checkbox.

  3. Click ![the Add SSH configuration](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) Add SSH configuration.

  4. In the SSH Configurations dialog, add a new configuration by doing the following:

     1. Click the Add button.

     2. In the Host and Port fields, specify the connection details of your jump host. For example, `my-jump-host.amazonaws.com`, `22`. 

     3. Enter your username in the Username field.

     4. In this tutorial, we use encrypted private key file and public key file to authenticate. From the Authentication type list, select Key pair. 

     5. To provide your private key file, click ![the Browse icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.browse.svg) Browse in the Private key file field and select the file.

For this authentication type, make sure that your public key file is provided and stored on the jump host.

     6. Specify your passphrase in the Passphrase field.

     7. Click Test Connection to run a test connection to the jump host.

[![SSH configuration and successful test connection to the jump host](https://resources.jetbrains.com/help/img/idea/2025.3/db_ssh_connection_example_config_cloud_success.png)](https://resources.jetbrains.com/help/img/idea/2025.3/db_ssh_connection_example_config_cloud_success.png)
     8. In the SSH Configurations dialog, click OK to confirm the new SSH configuration settings.

  5. On the General tab of the Data Sources and Drivers dialog, specify your database connection details:

     1. In the Host and Port fields, specify your database server address and port number. For example, `mysql-ssh.my-account.my-region.amazonaws.com` and `3306`. 

     2. From the Authentication dropdown, select User & Password.

     3. In the User and Password fields, type your user credentials.

     4. In the Database field, type the database name to which you want to connect. In our example, `testdb`.

     5. In the URL field, IntelliJ IDEA generates the JDBC URL automatically using the values of other connection settings.

If you need to use a JDBC URL with certain additional settings, paste it in the URL field. 

For example, `jdbc:mysql://my-endpoint.amazonaws.com:3306/testdb`. 

  6. Click the Test Connection link at the bottom of the connection details area to initiate a test connection to your database.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)
  7. Click OK to create the data source.


[![Connection settings of the MySQL \[Cloud, SSH\] data source](https://resources.jetbrains.com/help/img/idea/2025.3/db_ssh_connection_example_data_source_cloud.png)](https://resources.jetbrains.com/help/img/idea/2025.3/db_ssh_connection_example_data_source_cloud.png)
