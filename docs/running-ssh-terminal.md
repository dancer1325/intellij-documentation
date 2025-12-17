[//]: # (Source: https://www.jetbrains.com/help/idea/running-ssh-terminal.html)
[//]: # (Downloaded: 2025-12-17 19:59:27)

# Run SSH terminal

You can launch an SSH Session right from IntelliJ IDEA. By running commands in a dedicated SSH terminal, you can access data on a remote Web server or a Vagrant instance (virtual machine) via an SSH tunnel, mainly upload and download files.

### Enable the FTP/SFTP/WebDAV Connectivity plugin

This functionality relies on the [FTP/SFTP/WebDAV Connectivity](https://plugins.jetbrains.com/plugin/13125-ftp-sftp-webdav-connectivity) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The FTP/SFTP/WebDAV Connectivity plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the FTP/SFTP/WebDAV Connectivity plugin, and select the checkbox next to the plugin name.




### Set up the SSH terminal

  1. Make sure an SSH server is available in the destination environment: a remote Web server or a Vagrant instance (virtual machine).

  2. Register an account on the SSH server in the destination environment and generate a pair of SSH keys or a password, depending on the server policy.

  3. Appoint the destination environment and specify the settings to establish connection with it:

     1. In the Settings dialog (`Ctrl+Alt+S`) , go to Tools | SSH Terminal.

     2. In the Connection settings area, appoint the destination environment:

        * Current Vagrant: select this option to have the commands in the SSH Terminal executed on the currently running [Vagrant virtual machine](vagrant-support.html).

        * SSH configuration: select this option to have the commands in the SSH Terminal executed on the local or remote Web server accessible through one of the [SSH configurations](create-ssh-configurations.html).

          * Select SSH configuration on every run: if this option is selected, you will have to choose the desired configuration from the popup, every time you choose Tools | Start SSH Session from the main menu.

          * If the desired SSH configuration does not appear in the list, click the Set up configurations link, and define one in the [SSH Configurations](settings-tools-ssh-configurations.html) page.

     3. From the Default encoding list, select the desired encoding to be used in the SSH terminal.




### Launch the SSH terminal

  1. In the main menu, go to Tools | Start SSH Session. Alternatively, invoke the Help | Find Action `Ctrl+Shift+A` dialog, search for _start ssh.._ , and select Start SSH Session.

  2. Depending on the connection settings defined on the Tools | SSH Terminal page of the Settings dialog (`Ctrl+Alt+S`) , the following types of behavior are possible:

     * If the Current Vagrant option has been selected, the SSH Terminal will provide access to the currently running Vagrant virtual machine. 

For more information, refer to [Vagrant](vagrant-support.html).

     * If the SSH configuration option has been selected, the SSH Terminal will provide control over the data on the server accessible through the SSH configuration selected from the list. For more information, refer to [Create SSH configurations](create-ssh-configurations.html).

     * If the Select SSH configuration on every run option has been selected, IntelliJ IDEA will show a list to choose the desired SSH configuration from.

If no Vagrant virtual machine or SSH connection has been previously set up in IntelliJ IDEA, an SSH Session dialog opens prompting you to [create an SSH configuration](create-ssh-configurations.html).




### View SSH logs

SSH connections in IntelliJ IDEA run via [OpenSSH](https://www.openssh.com/), which maintains comprehensive logs both on the client and on the server. The exact location depends on your operating system.

For example, in Linux distributions that are based on Fedora, you should be able to see the logs by running `journalctl -u ssh`.




21 October 2025

[Create SSH configurations](create-ssh-configurations.html)[Tutorial: Deployment in IntelliJ IDEA](tutorial-deployment-in-product.html)
