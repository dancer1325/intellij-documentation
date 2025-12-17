[//]: # (Source: https://www.jetbrains.com/help/idea/code-with-me-security-overview.html)
[//]: # (Downloaded: 2025-12-17 19:20:53)

## Connection workflow

Let's say we have two users that want to connect to each other using Code With Me.

  1. A user (Host) clicks the Start Code With Me Session action to create a session in their local IDE.

![Start Session](https://resources.jetbrains.com/help/img/idea/2025.3/cwm_enable_access.png)

The local IDE sends a notification about the session creation to a lobby server, and asks for the session connection.

  2. After the registration, the link is created.

  3. The generated link is sent to another user (Guest) by any means that are available. 

For example, it can be sent via Slack, WhatsApp messenger, e-mail, and so on.

  4. The other user (Guest), clicks the received link.

  5. A guest receives parameters on how to connect to the host and starts connecting.

At this point, the authorization from the host is requested. If the host grants the access, the connection is continued, and the guest connects to a session.



