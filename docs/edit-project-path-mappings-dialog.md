[//]: # (Source: https://www.jetbrains.com/help/idea/edit-project-path-mappings-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:25:29)

# Edit Project Path Mappings dialog

The dialog opens when you click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) next to the Path Mappings field in the [Run/Debug Configuration: Node.js](run-debug-configuration-node-js.html) with a [remote Node.js runtime accessible via SSH](node-via-ssh.html). 

Path mappings for remote Node.js runtimes accessible via SFTP or located in [Docker containers](node-with-docker.html#ws_node_docker_create_run_debug_configuration) are retrieved automatically from the corresponding SFTP deployment configuration or Dockerfile. These mappings are read-only.

  * To add a custom mapping, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and specify the path in the project and the corresponding path on the remote runtime environment in the Local Path and Remote Path fields respectively. Type the paths manually or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select the relevant files or folders in the dialog that opens. 

![Create Node.js run configuration: add mapping](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_ssh_run_configuration_add_mapping.png)

Specify the paths to the local folders and the corresponding folders on the remote host. For example, you can map the project folder to /home/opc.

![Create Node.js run configuration: mapping added](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_ssh_run_configuration_mapping_added.png)
  * To remove a custom mapping, select it in the list and click ![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg).




06 November 2025

[Configure Node.js Remote Runtime Dialog](configure-node-js-remote-interpreter.html)[Run/Debug Configuration: Attach to Node.js/Chrome](run-debug-configuration-node-js-remote-debug.html)
