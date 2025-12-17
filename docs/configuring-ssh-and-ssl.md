[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-ssh-and-ssl.html)
[//]: # (Downloaded: 2025-12-17 19:22:03)

## SSL

The following procedure describes the SSL configuration that suits most databases. For some databases, you need to use another approach for a successful connection. You can see configuration examples for [Cassandra](https://www.jetbrains.com/help/datagrip/how-to-connect-to-cassandra-with-ssl.html) and [Heroku Postgres](https://www.jetbrains.com/help/datagrip/how-to-connect-to-heroku-postgres.html) in the DataGrip documentation.

### Connect to a database with SSL

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. Click the SSH/SSL tab and select the Use SSL checkbox.

  4. In the CA file field, navigate to the CA certificate file (for example, mssql.pem).

  5. You can leave the certificate file fields empty and use a truststore to obtain a required certificate from the certificates that it contains. To do that, tick the Use truststore checkbox and select the truststore that you want to use.

     * IDE: Use the certificates that are accepted by the IDE. You can add new accepted certificates in Settings | Appearance & Behavior | System Settings | Server Certificates.

     * JAVA: Use JAVA truststore certificates.

     * System: Use System truststore certificates.

  6. In the Client certificate file field, navigate to the client certificate file (for example, client-cert.pem).

  7. In the Client key file field, navigate to the client key file (for example, client-key.pem).

  8. From the Mode list, select the verification mode:

|   
---|---  
Require| Verifies that the server recognizes the client certificate, if the certificate is provided.  
Verify CA| 
     * Verifies that the server recognizes the client certificate, if the certificate is provided.
     * Verifies the server by checking the certificate chain up to the root certificate that is stored on the client.  
Full Verification| 
     * Verifies that the server recognizes the client certificate, if the certificate is provided.
     * Verifies the server by checking the certificate chain up to the root certificate that is stored on the client.
     * Verifies the server host to ensure that it matches the name stored in the server certificate.  
  
The SSL connection fails if either one of the certificates cannot be verified.

  9. To ensure that the connection to the data source is successful, click Test Connection.

![Connect to a database with SSL](https://resources.jetbrains.com/help/img/idea/2025.3/db_connect_with_ssl.png)



It is recommended to use PEM certificates.

With self-signed certificates and in some cases with certificates issued by the trusted root entity, you might experience errors when you use the latest JDBC driver version. The SSL connection might fail if your Java keystore does not accept the certificate chains. As a temporary solution, try to downgrade the JDBC driver (for example, for the MySQL connector, you need to switch to the 5.1.40 version.)

### Disable SSL connection to a database

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. Click the SSH/SSL tab and clear the Use SSL checkbox.

  4. Click Apply.




### Copy SSL settings from other data sources

If you configured SSL settings for one data source, you can copy them for another data source.

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. Click the SSH/SSL tab and select the Use SSL checkbox.

  4. Click the Copy from link and select the configuration that you want to copy.



