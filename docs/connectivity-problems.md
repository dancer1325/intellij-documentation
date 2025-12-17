[//]: # (Source: https://www.jetbrains.com/help/idea/connectivity-problems.html)
[//]: # (Downloaded: 2025-12-17 19:22:21)

## Step 1. Check your network settings

Databases can work locally, on a server, or in the cloud. For server and cloud databases, you need a network connection. To verify that the connection is available, use ping and telnet commands.

With the ping command, you can ensure that the destination computer is reachable from the source computer. Open a command line and type the following command: `ping -a <host_IP>`, where `-a` is a command option that resolves addresses to hostnames (if it is possible). If you use hostnames with the ping command, a hostname is resolved to the IP address. For example, `ping -a example.com` resolves to `PING example.com (93.184.216.34)`.

ping -a <host_IP>

![Test connection with the ping command](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_with_ping.png)

With the telnet command, you can test connectivity to remote computers and issue commands. If you specify a port as a parameter for the `telnet` command, you can test connectivity to a remote host on the given port. If the connection is successful, you see the message: `Connected to <host_IP>`.

telnet <host_IP> <port_number>

![Test connection with the telnet command](https://resources.jetbrains.com/help/img/idea/2025.3/db_test_connection_with_telnet.png)

For security reasons, DBMS usually drops all telnet connections. The telnet command allows you to check if the port is opened for communication.
