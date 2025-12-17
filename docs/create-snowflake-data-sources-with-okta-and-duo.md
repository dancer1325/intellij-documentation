[//]: # (Source: https://www.jetbrains.com/help/idea/create-snowflake-data-sources-with-okta-and-duo.html)
[//]: # (Downloaded: 2025-12-17 19:23:08)

## SSO using Okta

Before connecting to a Snowflake database with Okta SSO authentication, make sure to install and set up the [Okta Verify](https://help.okta.com/en-us/content/topics/mobile/okta-verify-overview.htm) application first.

Once the required software is set up and ready, you need to create a Snowflake data source in IntelliJ IDEA and configure it to use it with Okta SSO authentication. 

### Create a Snowflake data source to use with Okta

  1. In the Database tool window, click ![the New icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) New on the toolbar and navigate to Data Source | Snowflake. 

![Select the Snowflake data source](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_data_source_snowflake.png)
  2. Check if there is a Download missing driver files link at the bottom of the connection settings area. Click this link to download drivers that are required to interact with a database. 

![The Download missing driver files link](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_download_missing_drivers_link.png)
  3. Specify the database connection details. 

     1. In the Name field, enter your new data source name.

For example, `Snowflake [Okta]`.

     2. In the Host field, type the URL to connect to your Snowflake account with. For example, `myorg-myconnection.snowflakecomputing.com`.

     3. From the Authentication dropdown, select Authenticator.

     4. In the Authenticator field, type `externalbrowser`.

     5. In the User field, type the email address you use to log in to your Okta account.

     6. In the Password field, type your Okta account password.

     7. In the Database field, type the database name to which you want to connect. 

     8. In the Schema field, type the schema name to which you want to connect.

     9. In the Warehouse field, type the name of a compute resources cluster in Snowflake that you want to use. 

Alternatively, type your JDBC URL in the URL field. The general URL to use is as follows:

     * Format:

`jdbc:snowflake://<organization_name>-<connection_name>.snowflakecomputing.com/?warehouse=<warehouse_name>&db=<database_name>&schema=<schema_name>&user=<okta_username>&password=<okta_password>&authenticator=externalbrowser`

     * Example:

`jdbc:snowflake://myorg-myconnection.snowflakecomputing.com/?warehouse=AUTH_WH&db=TESTDB&schema=MYSCHEMA&user=MYUSERNAME@DOMAIN.COM&password=DUMMY-PASSWORD&authenticator=externalbrowser`

  4. Click the Test Connection link at the bottom of the connection details area to initiate a test connection to your database.

![Test Connection link](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_link.png)
  5. On the Okta website that opens in the browser, enter your user credentials and log in to your Okta account.

![Log in to your Okta account on the Okta website](https://resources.jetbrains.com/help/img/idea/2025.3/db_snowflake_okta_log_in_to_okta.png)
  6. Verify your identity using one of the available security methods.

![Verify your identity on the Okta website](https://resources.jetbrains.com/help/img/idea/2025.3/db_snowflake_okta_verify_identity.png)
  7. Once Okta confirms your identity, return to IntelliJ IDEA.

![Identity confirmation message from Okta](https://resources.jetbrains.com/help/img/idea/2025.3/db_snowflake_okta_verified.png)
  8. In the IDE, click OK to save your new data source.


![Database connection details](https://resources.jetbrains.com/help/img/idea/2025.3/db_connection_details_snowflake_okta_connection.png)
