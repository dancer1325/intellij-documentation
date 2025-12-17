[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-remote-node-interpreters.html)
[//]: # (Downloaded: 2025-12-17 19:22:00)

## Remote Node.js runtime on a host accessible through SSH connection

### Before you start

  1. Install the Node.js and Node.js Remote Interpreter plugins on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

  2. Make sure the FTP/SFTP/WebDAV Connectivity plugin is enabled in the settings. Press `Ctrl+Alt+S` to open settings and then select Plugins. Click the Installed tab. In the search field, type FTP/SFTP/WebDAV Connectivity. For more information about plugins, refer to [Managing plugins](managing-plugins.html). 

  3. Configure access to an SSH server on the target remote host as described in [Create SSH configurations](create-ssh-configurations.html) and make sure this server is running.




Node.js runtime via SSH are configured in the Configure Node.js Remote Interpreter dialog. You can open this dialog from the [JavaScript Runtime](javascript-runtime.html) page of the Settings dialog or later, when you [create or edit a Node.js run/debug configuration](#ws_node_configure_remote_interpreter_ssh_run_configuration) for running or debugging your application.

The recommended way is to configure a remote Node.js runtime in the Settings dialog. In this case you can set the runtime and the associated package manager as default for your project. 

A remote Node.js runtime that you configure right in the Node.js run/debug configuration can be used only with this run/debug configuration. 

### Configure a remote Node.js runtime via SSH in the Settings dialog

  1. Open the Settings dialog (`Ctrl+Alt+S`) and go to Languages & Frameworks | JavaScript Runtime. 

  2. Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) next to the Node runtime field. 

![Add runtime - Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_interpreter_from_settings_browse_button.png)
  3. In the [Node.js Runtimes](node-js-interpreters.html) dialog with a list of all the currently configured runtimes, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar and select Add Remote from the context menu.

![Configure Node.js runtime via SSH: Add Remote](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_interpreter_from_settings_docker_add_remote.png)
  4. In the [Configure Node.js Remote Runtime dialog](configure-node-js-remote-interpreter.html) that opens, select SSH. 

  5. Select an SSH configuration to use.

![Configure remote Node.js runtime via SSH: select SSH configuration](https://resources.jetbrains.com/help/img/idea/2025.3/ws_configure_remote_node_interpreter_ssh_select_ssh_configuration.png)

Alternatively, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and create a new SSH configuration as described in [Create SSH configurations](create-ssh-configurations.html).

  6. Click OK to return to the Node.js Interpreters dialog where the new runtime is added to the list. 

![Remote Runtimes dialog: the new Node.js runtime via SSH added to the list](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_node_configure_interpreter_remote_interpreters_dialog_ssh_node_added.png)
  7. To set the newly configured runtime as project default, select it in the list and click OK to return to the JavaScript Runtime dialog. 

IntelliJ IDEA automatically uses this interpreter every time you select the `Project` alias from Node runtime lists, for example, when creating run/debug configurations. 

To use the package manager associated with the new runtime for managing your project dependencies, set this package manager as default in your project. To do that, specify the location of the package manager in the Package manager field. 

The default location for npm executable is `/usr/local/lib/node_modules/npm`. 

![Configure Node.js runtime via SSH: set as default project interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_interpreter_from_settings_ssh_default_project_interpreter_and_package_manager.png)



### Configure a remote Node.js runtime via SSH in a run/debug configuration

  1. Go to Run | Edit Configurations. In the Edit Configuration dialog that opens, click ![the Add New Configuration button ](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar and select Node.js from the context menu. The [Run/Debug Configuration: Node.js](run-debug-configuration-node-js.html) dialog opens. 

  2. Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) next to the Node runtime field.

![Node.js run/debug configuration: file specified](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_ssh_configure_interpreter_run_configuration_new.png)

The [Node.js Runtimes](node-js-interpreters.html) dialog opens.

  3. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar and select Add Remote from the context menu.

![Node.js via SSH: run/debug configuration, configure runtime, select Add Remote](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_ssh_run_configuration_add_remote_new.png)
  4. Configure a remote Node.js runtime via SSH [as described above](#ws_node_ssh_configure_remote_interpreter_preferences_remote_interpreters_dialog).



