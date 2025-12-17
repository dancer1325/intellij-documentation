[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-ssh-terminal.html)
[//]: # (Downloaded: 2025-12-17 20:02:11)

# SSH Terminal

Use this dialog to appoint a remote Web server or a Vagrant instance (virtual machine) to access through the [SSH terminal](running-ssh-terminal.html), configure connection with the destination environment, and choose the encoding to use in the SSH terminal.

Use this dialog to configure the [SSH terminal](running-ssh-terminal.html).

Item| Description  
---|---  
Connection settings| In this section, appoint a remote Web server or a Vagrant instance (virtual machine) to access through the SSH terminal and specify where the connection settings should be taken from:

  * Current Vagrant: select this option to have the commands in the SSH Terminal executed on the currently running [Vagrant virtual machine](vagrant-support.html).
  * SSH configuration: select this option to have the commands in the SSH Terminal executed on the local or remote Web server accessible through one of the [SSH configurations](create-ssh-configurations.html).
    * Select SSH configuration on every run: if this option is selected, you will have to choose the desired configuration from the popup, every time you choose Tools | Start SSH Session from the main menu.
    * If the desired SSH configuration does not appear in the list, click the Set up configurations link, and define one in the [SSH Configurations](settings-tools-ssh-configurations.html) page.

  
Default encoding| From this list, select the desired encoding to be used in the SSH terminal.  
  
15 July 2025

[SSH Configurations](settings-tools-ssh-configurations.html)[Big Data Tools](big-data-tools-connections.html)
