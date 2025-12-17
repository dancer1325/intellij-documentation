[//]: # (Source: https://www.jetbrains.com/help/idea/cannot-connect-to-a-database-because-of-sslhandshakeexception.html)
[//]: # (Downloaded: 2025-12-17 19:19:37)

## MySQL

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. Select a data source for which you want to enable disabled algorithms (for example, MySQL 8.0.3). The following required algorithms might be disabled: `SSLv3`, `TLSv1`, `TLSv1.1`, `RC4`, `DES`, `MD5withRSA`, `DH keySize < 1024`, `EC keySize < 224`, `3DES_EDE_CBC`, `anon`, `NULL`, `include jdk.disabled.namedCurves`.

  3. In the right pane of a data source, click Test Connection.

  4. In the notification, select an action that you want to perform. You can select among the following actions:

     * Edit disabled algorithms: opens the Advanced tab of the selected data source and moves the focus to the VM options field. In the VM options field, you can edit a list of disabled algorithms manually (for the `Djdk.tls.disabledAlgorithms` option).

     * Enable TLSv1: removes `TLSv1` from the `Djdk.tls.disabledAlgorithms` option. This action will enable TLS 1.0.

     * Enable TLSv1.1: removes `TLSv1.1` from the `Djdk.tls.disabledAlgorithms` option. This action will enable TLS 1.1.

     * Enable all protocols in JDBC driver: removes `SSLv3`, `TLSv1`, `TLSv1.1`, `RC4`, `DES`, `MD5withRSA`, `DH keySize < 1024`, `EC keySize < 224`, `3DES_EDE_CBC`, `anon`, `NULL`, `include jdk.disabled.namedCurves` from the `Djdk.tls.disabledAlgorithms` option. This action enables all the disabled algorithms.

  5. Click Test Connection and see if the fix works.

You can try Enable TLSv1 and Enable TLSv1.1 first. If the error still occurs, try to enable other algorithms.

![javax.net.ssl.SSLHandshakeException](https://resources.jetbrains.com/help/img/idea/2025.3/db_javax_net_ssl_ssl_handshake_exception.png)


