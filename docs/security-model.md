[//]: # (Source: https://www.jetbrains.com/help/idea/security-model.html)
[//]: # (Downloaded: 2025-12-17 20:00:02)

## Connection security

The communication between JetBrains Client and the IDE backend is end-to-end encrypted with the 1.3 TLS even if performed in a secure SSH tunnel. JetBrains uses TLS 1.3 and on top of that, the SSH security connection is used.

Since in Remote Development there is no trust hierarchy from root certificates, the additional manual check is performed to ensure that there is no man-in-the-middle attack.

The regular connection link looks as follows:

tcp://0.0.0.0:5990#jt=71b0a870-e082-4e6b-aaf6-757398801cd2&p=IU&fp=17DC5CAB759FD8BB4298AF1116EA7D5E1F1D3C4D520CFC99748DBD0A88840B36&cb=223.2951&jb=17.0.4b535.2

  * Upon the connection, a client checks that the fingerprint of a host certificate is exactly `fp`. It verifies for the client that the host is correct (not hijacked by a third-party)

  * Upon the connection, a host checks that the client provides a one-time connection token `jt`. It denies connection for anyone on this port who does not know this token.




It is safe to transfer any authentication information via this connection or pass this connection data via public space. It is done the same way for [Code With Me](code-with-me-security-overview.html#connection_security) as well. 
