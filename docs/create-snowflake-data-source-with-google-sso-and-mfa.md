[//]: # (Source: https://www.jetbrains.com/help/idea/create-snowflake-data-source-with-google-sso-and-mfa.html)
[//]: # (Downloaded: 2025-12-17 19:23:05)

## SSO using Google Workspace

In this case, authentication is performed by logging into your Google account in a web browser window with your credentials.

### Create a Snowflake data source to use with Google Workspace SSO

  1. In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar and navigate to Data Source | Snowflake. 

![Select the Snowflake data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source_snowflake.png)
  2. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)
  3. Specify the database connection details. 

     1. In the Name field, enter your new data source name.

For example, `Snowflake [SSO]`.

     2. In the Host field, type the URL to connect to your Snowflake account with. For example, `myorg-myconnection.snowflakecomputing.com`.

     3. From the Authentication dropdown, select Authenticator.

     4. In the Authenticator field, type `externalbrowser`.

     5. In the User field, type the email address you use to log in to both your Snowflake and Google accounts. In Snowflake, it is your `login_name`.

     6. Leave the Password field empty.

You can set the Password field empty by right-clicking it and selecting Set Empty.

![the Set Empty context menu action](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_password_set_empty.png)
     7. In the Warehouse field, type the name of a compute resources cluster in Snowflake that you want to use. 

Alternatively, type your JDBC URL in the URL field. The general URL to use is as follows:

     * Format:

`jdbc:snowflake://<organization_name>-<connection_name>.snowflakecomputing.com/?warehouse=<warehouse_name>&db=<database_name>&schema=<schema_name>&user=<okta_username>&password=<okta_password>&authenticator=externalbrowser`

     * Example:

`jdbc:snowflake://myorg-myconnection.snowflakecomputing.com/?warehouse=AUTH_WH&db=TESTDB&schema=MYSCHEMA&user=MYUSERNAME@DOMAIN.COM&password=DUMMY-PASSWORD&authenticator=externalbrowser`

  4. Click the Test Connection link at the bottom of the connection details area to initiate a test connection to your database.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)
  5. On the Google website that opens in the browser, enter your user credentials and log in to your Google account.

![Log in to your Google account on the Google website](https://resources.jetbrains.com/help/img/idea/2025.3/db_snowflake_google_log_in_to_google.png)
  6. Once Google confirms your identity, return to IntelliJ IDEA.

![Identity confirmation message from Okta](https://resources.jetbrains.com/help/img/idea/2025.3/db_snowflake_google_sso_verified.png)
  7. In the IDE, click OK to save your new data source.


![Database connection details](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_details_snowflake_google_sso_connection.png)
