[//]: # (Source: https://www.jetbrains.com/help/idea/settings-docker-console.html)
[//]: # (Downloaded: 2025-12-17 20:00:52)

# Docker console settings

Configure the output of the [Docker container logs](https://docs.docker.com/config/containers/logging/). IntelliJ IDEA can show the log messages from the container's standard output streams in the Log tab when you select the container in the Services tool window (View | Tool Windows | Services or `Alt+8`). For more information, refer to [Container dashboard](services-tool-window.html#docker-container-dashboard).

### Enable the Docker plugin

This functionality relies on the [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Docker plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the Docker plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Docker plugin, and select the checkbox next to the plugin name.


![The Docker Console settings page](https://resources.jetbrains.com/help/img/idea/2025.3/settings_docker_console.png)

Fold previous sessions in the Log console
    

IntelliJ IDEA saves the console output of all container sessions. Select this option to fold output from previous sessions, leaving only the latest session's log expanded.

25 June 2025

[Docker Registry settings](settings-docker-registry.html)[Languages and Frameworks](settings-languages-and-frameworks.html)
