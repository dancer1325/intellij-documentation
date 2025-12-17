[//]: # (Source: https://www.jetbrains.com/help/idea/remote-development-troubleshooting.html)
[//]: # (Downloaded: 2025-12-17 19:57:13)

## Setup

Question| Answer  
---|---  
Is there a difference between JetBrains Gateway from Toolbox, the one downloaded separately, or the one from an IDE?| Standalone JetBrains Gateway supports an option to "Open in IDE" your [Space-based project](https://www.jetbrains.com/help/space/getting-started.html#what-is-space) If you don't use it, there are no other differences in installers and workflows.Check the [installation scenarios](jetbrains-gateway.html).  
Can I point Remote Development to an existing IDE on my remote server? Is it possible to install IDE manually?| Since version 221.5481, you can manually register an existing backend IDE on the remote server and make it visible for JetBrains Gateway. Installed IDE will appear in the list of available builds:

  1. Enter remote server by SSH.
  2. Locate the folder with unpacked IDE, enter the `bin` folder.
  3. In the command line, execute the following command: remote-dev-server.sh registerBackendLocationForGatewayFor example,sh IDEA-221.5591.52/bin/remote-dev-server.sh registerBackendLocationForGateway

  
The JetBrains Gateway installation itself doesn't finish successfully| 

  * Ensure your system user has permissions to install a software or contact a system administrator in your organization.

  
Why does the SSH connection to a remote server fail during the setup?| 

  * Firewall on the remote server side or the virtual machine provider prohibits incoming connection. In the case of AWS, don't forget to adjust "Security groups"
  * On the remote side, your SSH listens to a non-standard port
  * Password or key file is incorrect or your connection was blocked due to several failures

  
JetBrains Gateway hangs on the Retrieving IDE versions step and doesn't load available IDEs| 

  * JetBrains Gateway can't connect to [JetBrains' site](https://data.services.jetbrains.com/products) to fetch the list of existing builds

  
JetBrains Gateway tries to connect but fails. Credentials are 100% correct.| 

  * Ensure `AllowТcpForwarding` in `sshd_config` on the remote server is enabled as it's required for redirecting remote IDE process' traffic to your local machine.

  
I select an IDE installer from the local machine, but the process of uploading fails| 

  * The remote server doesn't have enough available space on the disk. The available space on your remote server must be at least 4xIDE.tar.gz in size.Since version 2022.1.1, you can select a custom path on the remote server as the deployment target location.
  * You uploaded not .tar.gz installer archive, so it can't be unpacked on the remote side
  * You uploaded a Community version's archive. Remote Development is available for paid versions.

  
Upload of remote-dev-worker fails with "exit code: 139 (SIGSEGV)"| If your remote machine's OS is RHEL, CentOS, RockyLinux - check syslog for SELinux warnings or disable SELinux and retry installation  
On local machine, the process fails with the "Failed to download JetBrains Client" error| Your local computer must have a network connection to the following JetBrains URLs:

  * https://code-with-me.jetbrains.com
  * https://download.jetbrains.com
  * https://download-cf.jetbrains.com
  * https://download-cdn.jetbrains.com
  * https://cache-redirector.jetbrains.com

Alternatively, you can configure the [fully offline mode](fully-offline-mode.html).
