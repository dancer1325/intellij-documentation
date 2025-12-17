[//]: # (Source: https://www.jetbrains.com/help/idea/db-tutorial-connecting-to-ms-sql-server.html)
[//]: # (Downloaded: 2025-12-17 19:24:10)

### Required settings

Microsoft SQL Server accepts TCP/IP connections on a dedicated port. By default, it is port `1433` and it is closed by the Microsoft Windows Firewall. When connecting via port, make sure that the Firewall does not close the port that you use.

If the [SQL Server Browser](https://docs.microsoft.com/en-us/sql/tools/configuration-manager/sql-server-browser-service?view=sql-server-2017) is turned on, TCP/IP connection can also be established using the Microsoft SQL Server instance name.

### Enable and configure the TCP/IP connection

  * Follow the [official instructions](https://learn.microsoft.com/en-us/sql/database-engine/configure-windows/configure-a-server-to-listen-on-a-specific-tcp-port?view=sql-server-ver16#assign-a-tcpip-port-number-to-the-sql-server-database-engine) to enable the protocol, check and assign a port number. Verify that other running applications do not use the same port.

Name of the Microsoft SQL Server instance is MSSQLSERVER. By default, the port is `1433`.




If you changed any settings, restart the server. For most situations, the restart resolves connection problems.
