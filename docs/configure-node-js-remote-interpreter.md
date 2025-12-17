[//]: # (Source: https://www.jetbrains.com/help/idea/configure-node-js-remote-interpreter.html)
[//]: # (Downloaded: 2025-12-17 19:21:32)

# Configure Node.js Remote Runtime Dialog

The following Node.js versions are supported in IntelliJ IDEA 2023.3 and later:

  * Node.js 22 - the Active Long Term Supported (LTS) version

  * Node.js 24 - the current version




Learn more from [Supported Node.js versions](supported-node-js-versions.html).

The dialog opens when you click Add ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) in the [Node.js Runtimes](node-js-interpreters.html) dialog and choose Remote... from the drop-down menu.

Use this dialog to configure access to Node.js installations on remote hosts or in development environments set up in Vagrant instances.

![Configuring a remote Node.js runtime on Docker](https://resources.jetbrains.com/help/img/idea/2025.3/ws_add_node_remote_docker.png)

Item| Description  
---|---  
SSH| Select this option to configure access to a Node.js runtime on a remote host or environment that is accessible through SSH credentials. Select the relevant SSH configuration and check the path to the default Node.js runtime from the remote host or environment.Learn more from [Create SSH configurations](create-ssh-configurations.html).  
Docker|  This option is available only when the Node.js, Node.js Remote Interpreter, and Docker Integration plugins are installed and enabled as described in [Installing plugins from the repository](managing-plugins.html#install_plugin_from_repo).Select this option to use a Node.js runtime in a Docker container.

  1. In the Server field, specify the Docker configuration to use. For more information, refer to [Configure the Docker daemon connection settings](docker.html#connect_to_docker). Select a configuration from the list or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and create a new configuration on the [Docker page](settings-docker.html) that opens. 
  2. In the Image name field, specify the base Docker image to use. Choose one of the previously downloaded or your custom images from the list or type the image name manually, for example, `node:argon` or `mhart/alpine-node`. When you later launch the run configuration, Docker will search for the specified image on your machine. If the search fails, the image will be downloaded from the [Docker Official Images](https://hub.docker.com/_/node/) repository on the [Docker Registry page](settings-docker-registry.html). 
  3. The Node.js runtime path field shows the location of the default Node.js runtime from the specified image.
  4. When you click OK, IntelliJ IDEA closes the Configure Node.js Remote Interpreter dialog and brings you to the [Node.js Runtimes](node-js-interpreters.html) dialog where the new runtime configuration is added to the list. Click OK to return to the run configuration.

  
Docker Compose|  This option is available only when the Node.js, Node.js Remote Interpreter, and Docker Integration plugins are installed and enabled as described in [Installing plugins from repository](managing-plugins.html#install_plugin_from_repo).Select this option to use a Node.js runtime configuration defined in a Docker Compose file docker-compose.yml. Note that this file must have `node` or `npm` in the `command` field, for example, `command: node ./src/app.js`. For more information, refer to the [Docker official website](https://docs.docker.com/compose/overview/).

  1. In the Server field, specify the Docker configuration to use. For more information, refer to [Configure the Docker daemon connection settings](docker.html#connect_to_docker). Select a configuration from the list or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and create a new configuration on the [Docker page](settings-docker.html) that opens. 
  2. In the Configuration file(s) field, specify the [docker-compose.yml file](https://docs.docker.com/compose/compose-file/) that defines the application's services.
  3. From the Service list, select the service you want to run. 
  4. Optionally, in the Environment variables field, define the environment variables. For more information, refer to [Docker Compose run configuration](docker-compose-run-configuration.html) settings.

  
Vagrant|  This option is available only when the Vagrant plugin is installed and enabled. The Vagrant plugin is not bundled with IntelliJ IDEA, but it can be installed on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). Choose this option to configure access to a Node.js runtime in a Vagrant instance using your Vagrant credentials. Technically, it is the folder where the VagrantFile configuration file for the desired environment is located. Based on this setting, IntelliJ IDEA detects the Vagrant host and shows it as a link in the Vagrant Host URL read-only field.  To use an interpreter configuration, you need path mappings that set correspondence between the project folders, the folders on the server to copy project files to, and the URL addresses to access the copied data on the server. IntelliJ IDEA evaluates path mappings from the VagrantFile configuration file.   
Node.js runtime path| In this field, specify the location of the Node.js executable file in accordance with the configuration of the selected remote development environment. 

  * For Vagrant instances, IntelliJ IDEA by default suggests the /usr/bin/node  location.
  * For Docker containers, IntelliJ IDEA by default suggests the node location.

To specify a different folder, click ![Open](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and choose the relevant folder in the dialog that opens. Note that the Node.js home directory must be open for editing.When you click OK, IntelliJ IDEA checks whether the Node.js executable is actually stored in the specified folder.

  * If no Node.js executable is found, IntelliJ IDEA displays an error message asking you whether to continue searching or save the interpreter configuration anyway.![No PHP executable found](https://resources.jetbrains.com/help/img/idea/2025.3/no-php-executable-found-message.png)
  * If the Node.js executable is found, you return to the Node.js Runtimes dialog where the installation folder and the detected version of the Node.js interpreter are displayed.

  
  
06 November 2025

[Node.js Runtimes Dialog](node-js-interpreters.html)[Edit Project Path Mappings dialog](edit-project-path-mappings-dialog.html)
