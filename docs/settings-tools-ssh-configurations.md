[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-ssh-configurations.html)
[//]: # (Downloaded: 2025-12-17 20:02:10)

## SSH configuration settings

Visible only for this project| Restrict this SSH configuration to the current project. The configuration will not be available in other projects. IntelliJ IDEA stores such configurations in the project's .idea directory, which you can share between team members [in a VCS](version-control-integration.html).By default, this option is disabled and IntelliJ IDEA stores the SHH configuration in the [IDE configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory). In this case, you can use this configuration in any project when working from the current instance of IntelliJ IDEA.  
---|---  
Host| Specify the hostname of the server to connect to. The default value is `localhost`.  
Username| Specify the username for authentication to the server.  
Port| Specify the remote port number to connect to. The default value is `22` (the standard TCP port for SSH).  
Authentication type| Select the client authentication method:

  * Password: Authenticate with the specified password and remember it if necessary.
  * Key pair: Use [SSH authentication](http://www.ssh.com/) with a key pair (OpenSSH or PuTTY). Specify the location of the private key file and the corresponding authentication passphrase. The public key should be on the remote server. Remember the passphrase if necessary.
  * OpenSSH config and authentication agent: Use a credentials helper application that manages your SSH keys, such as [ssh-agent](https://en.wikipedia.org/wiki/Ssh-agent).For example, see the following tutorial: [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

  
Parse config file ~/.ssh/config| Read the [OpenSSH client-side configuration file](https://www.ssh.com/academy/ssh/config) for any options not specified in the SSH configuration for the corresponding host.This option is available only for Password and Key pair authentication types. With OpenSSH config and authentication agent, IntelliJ IDEA reads the OpenSSH config file in any case.For more information, refer to [Supported OpenSSH directives](create-ssh-configurations.html#openssh-directives), [Run SSH terminal](running-ssh-terminal.html).  
Test Connection| Try to connect with the current SSH configuration settings.  
  
### Connection Parameters

Send keep-alive messages every| Send regular packets to keep the SSH connection active. Without regular messages, the remote server might close the connection. Set the message period in seconds.  
---|---  
Strict host key checking| Specify how to handle new and changed host keys.

  * Yes: Never add new host keys to the user's known_hosts file and never allow connections to hosts with changed host keys.
  * Accept New: Always add new host keys to the user's known_hosts file but never allow connections to hosts with changed host keys.
  * No: Always add new host keys to the user's known_hosts file and allow connections to hosts with changed host keys.
  * Ask: Add new host keys to the user's known_hosts file only after confirmation and never allow connections to hosts with changed host keys. This is the default behavior.

  
Hash hosts in knownhosts file| Store new host records in hash format.
