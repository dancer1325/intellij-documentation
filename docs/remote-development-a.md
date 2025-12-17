[//]: # (Source: https://www.jetbrains.com/help/idea/remote-development-a.html)
[//]: # (Downloaded: 2025-12-17 19:57:09)

## JetBrains Gateway

JetBrains Gateway is a lightweight launcher that connects a remote server with your local machine, downloads necessary components on the backend, and opens your project in JetBrains Client.

Refer to the quick video on how to start working with JetBrains Gateway.

You can use JetBrains Gateway as a standalone launcher or as an entry point from your IDE to connect to a remote server.

### Launch JetBrains Gateway and connect to a remote server

  1. Use one of the [installation scenarios](jetbrains-gateway.html) to open the Remote Development wizard.

  2. Сlick New Connection under the SSH connection provider.

![Connect via SSH](https://resources.jetbrains.com/help/img/idea/2025.3/all_providers.png)

You can also click Connect with a Link and enter a link that you previously [generated](#use_local_ide) to connect either to a Code With Me session or to a remote server.

  3. On the next page of the wizard, specify the SSH configuration through which you want to connect to a remote server.

![SSH settings](https://resources.jetbrains.com/help/img/idea/2025.3/ssh_settings.png)

Alternatively, click ![SSH configurations](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) to open the SSH Configurations dialog and configure the SSH settings.

In the SSH Configurations dialog, add the following information:

![SSH configurations](https://resources.jetbrains.com/help/img/idea/2025.3/ssh_configuration.png)
     * Host: specify the address of your remote server.

     * Port: specify the SSH port, which defaults to `22`.

     * Username: specify the name of a user that will be used to connect to the remote server.

     * Authentication type: select one of the following authentication methods:

       * Password: to access the host with a password. To save the password in IntelliJ IDEA, select the Save password checkbox.

       * Key pair (OpenSSH or PuTTY): to use [SSH authentication](https://www.ssh.com/) with a key pair. To apply this authentication method, you must have a private key on the client machine and a public key on the remote server. IntelliJ IDEA supports private keys that are generated with the [OpenSSH](https://www.openssh.com/) utility. 

Specify the path to the file where your private key is stored and type the passphrase (if any) in the corresponding fields. To have IntelliJ IDEA remember the passphrase, select the Save passphrase checkbox.

       * Parse config file ~/.ssh/config: select this option if you want JetBrains Gateway to use the `.ssh/config` file.

     * Test Connection: click this button to see whether the connection is established.

     * Connection Parameters: use this section to configure additional parameters for the connection. 

For more information, refer to [Connection Parameters](settings-tools-ssh-configurations.html#connection-parameters).

     * HTTP/SOCKS Proxy: use this section to configure proxy settings. For more information, refer to [Proxy settings](settings-http-proxy.html). 

Click OK to save the changes and return to the Welcome to JetBrains Gateway dialog.

Click Check Connection and Continue to check whether the connection is established.

  4. On the next page, specify the IntelliJ IDEA version to download to the remote server. JetBrains Gateway displays a list of the IDEs versions that are available for downloading and the already installed ones.

You can also use "Other options" for setting the alternative sources of [IDE installers](remote-development-starting-page.html#connect_to_rd_ij).

The version of JetBrains Client downloaded to your local machine always matches the remote IDE version.


![the IDE version](https://resources.jetbrains.com/help/img/idea/2025.3/ide_version.png)

By default, the downloaded IntelliJ IDEA is located in the following folder on the remote server: ~/.cache/JetBrains/RemoteDev/dist. However, you can change it and install IntelliJ IDEA into a custom location with the following steps:

  1. Click Other options and select the Customize install path option.

  2. In the Install path field add the needed location for the installation.


![Install to custom location](https://resources.jetbrains.com/help/img/idea/2025.3/rd_install_to_custom_location.png)

Add the path to your project on the remote host.

![Path to remote project](https://resources.jetbrains.com/help/img/idea/2025.3/path_to_remote_project.png)

Click Upload IDE and Connect.

JetBrains Gateway downloads the IDE, and opens your remote project in JetBrains Client. The connection is shown in the JetBrains Gateway window, from which you can connect to other IDEs or disable the connection. This window is hidden to tray by default.

![Gateway window](https://resources.jetbrains.com/help/img/idea/2025.3/gateway_window.png)

You can override the `-Xmx` VM options for the backend before you open your project.

### Override -Xmx VM options

  1. [Launch](#launch_gateway) JetBrains Gateway.

  2. Follow the steps of the wizard. Click Check Connection and Continue.

  3. On the page that opens, under the IDE version field, click Installation options.

  4. From the drop-down list, select Customize heap size. 

![Customize_heap_size](https://resources.jetbrains.com/help/img/idea/2025.3/customize_heap_size.png)
  5. In the Maximum heap size field, override the default heap size as needed.

![Maximum heap size](https://resources.jetbrains.com/help/img/idea/2025.3/max_heap_size.png)

Note that this field can only contain numeric values and cannot exceed the `INT_MAX` value.

If you want to return to the default value, click Installation options again and select Use default heap size.

  6. After you've done with your configurations, click Download IDE and Connect to start your project.




### Open recent projects

  1. In the JetBrains Gateway wizard, select SSH from the options on the left.

  2. In the search field, enter the name of your project to quickly navigate to it.

![Recent projects](https://resources.jetbrains.com/help/img/idea/2025.3/recent_projects.png)

If you need to quickly access the terminal, click ![Open terminal](https://resources.jetbrains.com/help/img/idea/2025.3/terminal.icons.OpenTerminal_13x13.svg).




### Change the backend version

  * In the JetBrains Gateway wizard, click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg) next to the name of the recent project and choose the version of the backend with which you want to open your project.

![Change the backend version](https://resources.jetbrains.com/help/img/idea/2025.3/change_backend_version.png)

If you can't locate the necessary version in the list, click Select Different IDE and choose the desired IDE version in the IDE version field.

![Select the IDE version](https://resources.jetbrains.com/help/img/idea/2025.3/select_ide_version.png)



### Stop the running instance

  1. In the JetBrains Gateway wizard, select SSH from the options on the left.

  2. When your remote session is active, the Running indicator is displayed next to the project.

![Running instance](https://resources.jetbrains.com/help/img/idea/2025.3/active_instance.png)

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.moreHorizontal.svg) next to the project and select Stop IDE Backend to stop the remote session for that project.

![Stop IDE Backend](https://resources.jetbrains.com/help/img/idea/2025.3/stop_instance.png)

You can also select Remove from Recent Projects to remove the project listed on the page altogether.




### Uninstall the backend IDE version

  1. In the JetBrains Gateway wizard, click ![the Show Options Menu icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) against the name of the remote server and select Manage IDE Backends to open the list of installed IDE versions.

![Manage IDE](https://resources.jetbrains.com/help/img/idea/2025.3/manage_ide.png)
  2. In the window that opens, click ![the Close icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.close.svg) next to the backend IDE version you need to uninstall and click Yes to confirm the action.



