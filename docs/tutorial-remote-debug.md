[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-remote-debug.html)
[//]: # (Downloaded: 2025-12-17 20:04:46)

## Overview

Remote debugging lets you control and inspect a Java program running on another machine as if it were local.

To do this, you first start the application on the remote computer and configure it to accept debugger connections by adding a special VM option. This option makes the remote JVM wait for incoming connections from a debugger.

Once the remote app is up and listening, you use your local machine to start a debugger in “attach” mode. This connects the IntelliJ IDEA's debugger to the remote application over the network, allowing you to debug it.

For simplicity, we will launch the debugger and the host application on the same computer. The steps, however, are identical for debugging that is actually remote, so you will be able to use the same procedure for both scenarios.
