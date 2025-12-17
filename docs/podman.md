[//]: # (Source: https://www.jetbrains.com/help/idea/podman.html)
[//]: # (Downloaded: 2025-12-17 19:34:03)

# Podman

[Podman](https://podman.io/) is a daemonless container manager that can run containers as root or in rootless mode. Podman commands are fully compatible with Docker, so you can replace one with the other: `alias docker=podman`.

The core Podman runtime environment can only run on Linux operating systems. However, you can use a [remote client](https://github.com/containers/podman/blob/main/docs/tutorials/mac_win_client.md) for other operating systems to manage containers on the machine running Podman. This topic describes how IntelliJ IDEA can act as a remote client for Podman.

### Enable the Docker plugin

This functionality relies on the [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Docker plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the Docker plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Docker plugin, and select the checkbox next to the plugin name.




### Run Podman

Starting from Podman version 3.2.0, you can use the [`podman machine`](https://docs.podman.io/en/latest/markdown/podman-machine.1.html) set of commands to run a virtual machine with Podman.

  1. [Install Podman](https://podman.io/docs/installation).

  2. Complete the following step based on your OS:

Initialize a new virtual machine:

podman machine init --rootful=true 

For more information, see [podman machine init](https://docs.podman.io/en/latest/markdown/podman-machine-init.1.html).

Next, start the Podman virtual machine:

podman machine start 

For more information, see [podman machine start](https://docs.podman.io/en/latest/markdown/podman-machine-start.1.html).

No virtual machine is needed. Use Podman directly after the installation.




If successful, the output will contain a URL of the Podman API and the `DOCKER_HOST` variable with a value that you can use for [connecting to Podman from IntelliJ IDEA](#connect) or any other Docker client. For example:

unix:///var/folders/3p/qnvz_wss4g32qcwxcmvsk70c0000gp/T/podman/podman-machine-default-api.sock 

### Connect to Podman from IntelliJ IDEA

For information about running Podman, see [Run Podman](#run).

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Docker.

  2. Click ![The Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add a Docker configuration.

  3. Select Podman and then select the name of the [Podman machine](https://podman-desktop.io/docs/podman/creating-a-podman-machine) in the Podman connection list.

If everything is correct, you should see Connection successful at the bottom of the page.




For more information, refer to [Docker connection settings](settings-docker.html).

### Troubleshoot Podman Linux connection error

If the connection to Podman could not be established, IntelliJ IDEA shows an error indicating that the Podman executable was found, but the connection to the Podman socket failed.

You can refer to [Podman documentation](https://docs.podman.io/en/latest/markdown/podman-system-service.1.html) for more details and use the following steps to troubleshoot the issue:

Configure the `systemd` socket to start automatically after a reboot and run as the specified user:

systemctl --user enable podman.socket loginctl enable-linger <USER>

Start the `systemd` socket for the service as root:

sudo systemctl start podman.socket 

Configure the socket to be automatically started after the reboot:

sudo systemctl enable podman.socket 

To run Dev Containers with Podman, set the `service_timeout=0` field in the `containers.conf` file.

  * This field is mentioned in the [Podman System Service](https://docs.podman.io/en/latest/markdown/podman-system-service.1.html) documentation under the `--time`, `-t` option description.

  * See the [complete specification](https://github.com/containers/common/blob/main/docs/containers.conf.5.md) of the `containers.conf` configuration file.







20 November 2025

[Docker troubleshooting](docker-troubleshooting.html)[MCP Server](mcp-server.html)
