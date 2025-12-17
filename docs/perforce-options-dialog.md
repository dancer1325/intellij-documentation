[//]: # (Source: https://www.jetbrains.com/help/idea/perforce-options-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:33:49)

# Perforce Options dialog

In this dialog, configure connection to the specified Perforce server.

Item| Description  
---|---  
Perforce is online| Select this checkbox to enable establishing connection to the Perforce server. If there is a connection but the server does not respond (for example, because the server is backing up currently), you can disable such attempts by clearing this checkbox, or IntelliJ IDEA will suggest to do that after a timeout. After that the version control-specific operations will be disabled.  
Use P4CONFIG or default connection| Use server information and user credentials from the P4CONFIG environment variable or default Perforce client connection. Otherwise, specify port, user, client, and password.  
Charset| Select the charset corresponding to the one set on the server.  
Dump Perforce commands to _IDEA_Home\bin\p4.output_|  Log Perforce commands in the specified file.  
Use login authentication| Toggle authentication.  
Try to log in silently| Skip prompt dialog. This option works when login authentication is required.  
Use native Perforce API| Speed up connection to the server using a special library.  
Path to P4 executable| Specify the path to the Perforce client executable file.  
Test connection| Make sure that connection to the Perforce server is established.  
Show branching history| See branches for files in the dialogs showing File History. When you work with several branches, it is recommended to enable this option so that the file branches are correctly displayed.  
  
If you use the [AI Assistant](https://plugins.jetbrains.com/plugin/22282-jetbrains-ai-assistant) plugin, you can also configure a [Perforce MCP server](https://github.com/perforce/p4mcp-server) in IntelliJ IDEA to give AI Assistant access to Perforce tools and data.

Learn more in the official [AI Assistant documentation](https://www.jetbrains.com/help/ai-assistant/ai-in-vcs-integration.html#configure-a-perforce-mcp-server).

04 November 2025

[Link Job to Changelist dialog](link-job-to-changelist-dialog.html)[Update Project dialog (Perforce)](update-project-dialog-perforce.html)
