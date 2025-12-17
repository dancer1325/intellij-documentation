[//]: # (Source: https://www.jetbrains.com/help/idea/docker-run-targets.html)
[//]: # (Downloaded: 2025-12-17 19:25:12)

# Docker run targets

Docker is great for running and debugging your application, because you can replicate any environment in a container. For example, the reporter of an issue may provide you with a specific Docker image where they are able to reproduce the problem. To run or debug your application in a Docker container, you can use [Run targets](run-targets.html).

### Create a Docker run target

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Run Targets. 

  2. Click ![The Add Target On button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Docker.

  3. Configure and create the Docker target as described in [Run Targets: Docker](run-targets.html#docker).


![Docker run target](https://resources.jetbrains.com/help/img/idea/2025.3/docker_run_targets.png)

### Run or debug your application on a Docker run target

  * Create a new [run or debug configuration](run-debug-configuration.html) for your application or configure an existing one to use the Docker run target.


![Java application with Docker run target](https://resources.jetbrains.com/help/img/idea/2025.3/application_run_configuration_with_docker_run_target.png)

For a specific example, refer to [Run and debug a Java application with Docker](running-a-java-app-in-a-container.html).

11 October 2024

[Docker compose run configuration](docker-compose-run-configuration.html)[Docker Compose](docker-compose.html)
