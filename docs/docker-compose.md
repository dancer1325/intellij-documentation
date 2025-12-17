[//]: # (Source: https://www.jetbrains.com/help/idea/docker-compose.html)
[//]: # (Downloaded: 2025-12-17 19:25:06)

# Docker Compose

[Docker Compose](https://docs.docker.com/compose/overview/) is used to run multi-container applications. For example, you can run a web server, a backend database, and your application code as separate services. Each service can be scaled by adding more containers if necessary. This enables you to perform efficient development and testing in a dynamic environment, similar to production.

### Enable the Docker plugin

This functionality relies on the [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Docker plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the Docker plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Docker plugin, and select the checkbox next to the plugin name.




IntelliJ IDEA recognizes [Docker Compose files](https://docs.docker.com/compose/compose-file/) and marks them with the ![](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-docker-impl.icons.expui.dockerCompose.svg) icon. It also adds [gutter icons](editor-gutter.html#gutter-action-icons) to run various services defined in the Docker Compose file.

![Docker Compose file](https://resources.jetbrains.com/help/img/idea/2025.3/docker_compose_file.png)

### Run a multi-container Docker application

  1. Define necessary services in one or several [Docker Compose files](https://docs.docker.com/compose/compose-file/).

  2. In the main menu, go to Run | Edit Configurations.

  3. Click ![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), point to Docker and then click Docker Compose.

![Docker Compose run configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/docker-compose-run-config.png)
  4. Specify the Docker Compose files with your service definitions. If necessary, you can define the services that this configuration will start, specify [environment variables](https://docs.docker.com/compose/environment-variables/), and force building of images before starting corresponding containers (that is, add the `--build` option for the [docker compose up](https://docs.docker.com/compose/reference/up/) command).

For more information about the available options, refer to [Docker compose run configuration](docker-compose-run-configuration.html).

  5. Click OK to save the Docker Compose run configuration, select it in the main toolbar and click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) or press `Shift+F10` to start the configuration.




To quickly create a Docker Compose run configuration and run it with default settings, right-click a Docker Compose file in the Project tool window and click Run in the context menu. You can also use gutter icons and the context menu in the Docker Compose file to run and manage services.

When Docker Compose runs your multi-container application, you can use the [Services](services-tool-window.html#docker) tool window to control specific services and [interact with containers](docker-containers.html#interacting-with-containers). The containers that run as part of Docker Compose are listed under the dedicated Compose nodes, not under the Containers node (which is only for standalone containers).

### Scale a service

  1. In the Services tool window, select the service you want to scale and click ![The Scale button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.expandAll.svg) or select Scale from the context menu.

  2. In the Scale dialog, specify how many containers you want for this service and click OK. 




### Stop a running service

  * In the Services tool window, select the service and click ![The Stop button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.suspend.svg) or select Stop from the context menu.




### Stop all running services

  * In the Services tool window, select the Compose node and click ![The Stop button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.suspend.svg) or select Stop from the context menu.




### Bring your application down

  * In the Services tool window, select the Compose node and click ![The Down button](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.undeploy.svg) or select Down from the context menu.




This stops and removes containers along with all related networks, volumes, and images.

### Open the Docker Compose file that was used to run the application

  * In the Services tool window, right-click the Compose node or a nested service node and then click Jump to Source in the context menu or press `F4`.




21 October 2025

[Docker run targets](docker-run-targets.html)[Run a database in a Docker container](running-a-dbms-image.html)
