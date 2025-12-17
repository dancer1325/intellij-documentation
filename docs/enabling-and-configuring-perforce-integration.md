[//]: # (Source: https://www.jetbrains.com/help/idea/enabling-and-configuring-perforce-integration.html)
[//]: # (Downloaded: 2025-12-17 19:25:42)

# Configure Perforce integration

The Perforce Integration is disabled by default. If you want to perform Perforce-related operations right from IntelliJ IDEA, enable the integration at the IDE level and associate the project root or specific directories with Perforce. The general procedure is described in the section [Version control integration support](enabling-version-control.html).

### Enable Perforce for a project or directory

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | Directory Mappings.

  2. Click the Add button ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the right.

  3. In the Add VCS Directory Mapping dialog that opens, select the necessary option (Directory or Project).

  4. Type the path to the directory that you want to associate with a version control system, or click the Browse button ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select the directory in the dialog that opens.

  5. From the VCS list, select Perforce.

  6. Apply the changes and close the dialog. 


![Enabling Perforce integration for directory](https://resources.jetbrains.com/help/img/idea/2025.3/enable-perforce-integration.png)

If you specify a wrong client workspace, and your project roots do not match with the workspace roots, IntelliJ IDEA displays a popup with a warning. Click Inspect in the popup to view and fix the discrepancies.

### Configure Perforce integration settings

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | Perforce.

  2. Select the Perforce is online checkbox to establish live connection to the Perforce server.

  3. Specify which credentials you want to use for connecting to the Perforce server.

     * To use the connection settings from your P4CONFIG files, choose the Use P4CONFIG or default connection option.

If you are using P4CONFIG files for configuration, IntelliJ IDEA shows what config files it has found and what other default settings are used. This way you can be sure that your P4CONFIG files are detected and taken into account.

     * To configure connection manually, choose the Use connection parameters option and specify the following settings in the corresponding fields:

       1. The Port the Perforce client will listen to.

       2. The Client.

       3. Your User name and Password to authenticate to the server.

  4. To use ticket-based authentication, select the Use login authentication checkbox. Otherwise, password-based authentication will be used. In either cases IntelliJ IDEA uses the login name and password specified in the dialog or stored in the P4CONFIG files.

  5. To have IntelliJ IDEA create a P4.output file and store the output of Perforce commands in it, select the Dump Perforce Commands to checkbox.

  6. Specify the path to the Perforce executable file. Click Test Connection to make sure your settings ensure successful connection.

  7. In the Timeout field, specify the lapse of time in seconds during which IntelliJ IDEA waits for response from the server. If the server does not respond in due time, the user is prompted to disable integration.

  8. To enable displaying the branch history of a specified file, including all file branch points, edits, and merges, select the Show branching history checkbox.

  9. To have IntelliJ IDEA point at committed changes that are also integrated to other changelists and provide information on the target changelists that received the content, select the Show integrated changelists in committed changes checkbox.

  10. To get the user interface for attaching and detaching Perforce jobs to changelists, select the Enable Perforce Jobs support checkbox.




You will know that the Perforce integration has been enabled once you close the settings: you will see the Perforce tool window at the bottom of your IDE window.

If you use the [AI Assistant](https://plugins.jetbrains.com/plugin/22282-jetbrains-ai-assistant) plugin, you can also configure a [Perforce MCP server](https://github.com/perforce/p4mcp-server) in IntelliJ IDEA to give AI Assistant access to Perforce tools and data.

Learn more in the official [AI Assistant documentation](https://www.jetbrains.com/help/ai-assistant/ai-in-vcs-integration.html#configure-a-perforce-mcp-server).

04 November 2025

[Perforce](using-perforce-integration.html)[Handle modified without checkout files](handling-modified-without-checkout-files.html)
