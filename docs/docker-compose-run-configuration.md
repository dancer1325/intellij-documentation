[//]: # (Source: https://www.jetbrains.com/help/idea/docker-compose-run-configuration.html)
[//]: # (Downloaded: 2025-12-17 19:25:05)

# Docker compose run configuration

Use this type of configuration to run multi-container Docker applications.

![Docker Compose run configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/docker-compose-run-config.png)

Docker uses the [docker compose](https://docs.docker.com/compose/reference/) command to define, configure, and run multi-container applications. The main command that builds, creates, starts, and attaches to containers is [docker compose up](https://docs.docker.com/compose/reference/up/).

By default, IntelliJ IDEA assumes that you are running Compose V2. However, if you are running the discontinued Compose V1, then the `docker compose` command will not work. In this case, you need to manually specify the location of the `docker compose` executable in [Docker connection settings](settings-docker.html).

For more information, see [Migrate to Compose V2](https://docs.docker.com/compose/migrate/).

By default, the Docker Compose configuration has the following options:

Item| Description  
---|---  
Name| Specify a name for the run configuration to quickly identify it among others when editing or running.  
Allow multiple instances| Allow running multiple instances of this run configuration in parallel.By default, it is disabled, and when you start this configuration while another instance is still running, IntelliJ IDEA suggests stopping the running instance and starting another one. This is helpful when a run configuration consumes a lot of resources and there is no good reason to run multiple instances.  
Store as project file| Save the file with the run configuration settings to share it with other team members. The default location is .idea/runConfigurations. However, if you do not want to share the .idea directory, you can save the configuration to any other directory within the project.By default, it is disabled, and IntelliJ IDEA stores run configuration settings in .idea/workspace.xml.  
Server| Select the [Docker daemon connection](docker.html#connect_to_docker) to use for the run configuration.  
Compose files| Specify the compose files that define the necessary services. Docker Compose builds the configuration in the specified order, so any subsequent files override and add to the fields of the same service in previous files.This is similar to using the `-f` option with the `docker compose` command.  
Services| Specify the services to build, create, and start.Click ![The Browse icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to select services that are listed in the YML file.![docker-compose browse icon](https://resources.jetbrains.com/help/img/idea/2025.3/db_docker_compose_browse_icon.png)  
Before launch| Specify a list of tasks to perform before starting the run configuration. For example, run another configuration, build the necessary artifacts, run some external tool or a web browser, and so on.Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or press `Alt+Insert` to add one of the available tasks.Move tasks in the list using ![the Up button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg) and ![the Down button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg) to change the order in which to perform the tasks. Select a task and click ![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) to edit the task. Click ![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) to remove the selected task from the list.  
Show this page| Show the run configuration settings before actually starting it.  
Activate tool window| Depending on the type of configuration, open the [Run](run-tool-window.html), [Debug](debug-tool-window.html), or [Services](services-tool-window.html) tool window when you start this run configuration. If this option is disabled, you can open the tool window manually:

  * View | Tool Windows | Run or `Alt+4`
  * View | Tool Windows | Debug or `Alt+5`
  * View | Tool Windows | Services or `Alt+8`

  
  
Use the Modify options menu to add advanced options to the run configuration:

Item| Description  
---|---  
Specify project name| Specify an alternative project name for Docker Compose. By default, it is the name of the current directory.This is similar to using the `-p` option with the `docker compose` command.  
Profiles| Specify [profiles](https://docs.docker.com/compose/how-tos/profiles/) for different environments or use cases in your application.Profiles let you group services and activate them only when needed, allowing a single compose.yml file to support multiple scenarios (for example, development, debugging, or production).You can specify multiple profiles; use commas to separate them.  
Environment variables| Specify the [Docker Compose environment variables](https://docs.docker.com/compose/reference/envvars/). These are used only by the Docker Compose process. They are not passed on to any of the containers.  
Environment variables file| Specify the path to a custom [environment file](https://docs.docker.com/compose/env-file/) that defines the [Docker Compose environment variables](https://docs.docker.com/compose/reference/envvars/).This is similar to using the `--env-file` option with the `docker compose` command.By default, the Docker Compose run configuration looks for a file named .env in the directory with the Docker Compose file.  
Enable compatibility mode| Convert v3 service definitions into v2 compatible parameters.This is similar to using the `--compatibility` option with the `docker compose` command.  
Remove orphans on `down| Remove containers for services that are not defined in the current Compose file when bringing the application down.  
Remove volumes on `down| When stopping and removing containers, also delete named volumes declared in the Docker Compose file and anonymous volumes attached to containers.This is similar to using the `-v` or `--volumes` option with the `docker compose down` command.  
Remove images on `down| Configure which images should be removed when stopping and removing containers. You can choose to remove all images used by any service or only images that don't have a custom tag set in the `image` field.This is similar to using the `--rmi` option with the `docker compose down` command.  
SIGKILL timeout| Set a timeout in seconds to forcefully terminate containers that do not shut down gracefully.Docker first attempts a graceful shutdown using `SIGTERM`, but a container may continue running indefinitely. Set a timeout after which Docker should issue `SIGKILL` to force the shutdown.This is similar to using the `-t` or `--timeout` option with the `docker compose up` command.  
Return exit code| Return the exit code of the selected service container.Whenever a container in the selected service stops, return its exit code and stop all other containers in the service.This is similar to using the `--exit-code-from` and `--abort-on-container -exit` options with the `docker compose up` command.  
Override scale| Set the number of containers to start for each service.This option overrides the `scale` parameter in the Docker Compose file, if it's present.This is similar to using the `--scale` option with the `docker compose up` command.  
Recreate dependencies| Recreate dependent containers when starting a service.This is similar to using the `--always-recreate-deps` option with the `docker compose up` command.  
Recreate anonymous volumes| Recreate anonymous volumes instead of retrieving data from the previous containers.This is similar to using the `-V` or `--renew-anon-volumes` option with the `docker compose up` command.  
Remove orphans| Remove containers for services not defined in the Docker Compose file.This is similar to using the `--remove-orphans` option with the `docker compose up` command.  
Don't print prefix in logs| Disable the service name prefix in log output to produce cleaner and simpler logs.  
Start| Configure which services to start:

  * Selected and dependencies: By default, Docker Compose starts all of the specified services and linked services.
  * None: Don't start any services after creating them. This is similar to using the `--no-start` option with the `docker compose up` command.
  * Selected services: Don't start any of the linked services. This is similar to using the `--no-deps` option with the `docker compose up` command.

  
Attach to| Configure for which containers to show output streams:

  * Selected services: By default, Docker Compose attaches to all started containers of the specified services.
  * None: Don't attach to any containers. This is similar to using the `-d` or `--detach` option with the `docker compose up` command.
  * Selected and dependencies: Attach to containers of the specified services and linked services. This is similar to using the `--attach-dependencies` option with the `docker compose up` command.

  
Recreate containers| Configure which containers to stop and replace by new ones:

  * Changed configuration: By default, Docker Compose recreates containers only if the corresponding configuration or image has changed.
  * All: Recreate all containers in the services, even if the corresponding configuration or image hasn't changed. This is similar to using the `--force-recreate` option with the `docker compose up` command.
  * None: Don't recreate any containers in the services, even if the corresponding configuration has changed. This is similar to using the `--no-recreate` option with the `docker compose up` command.

  
Build| Configure which images to build before starting containers:

  * Only missing images: By default, Docker Compose only builds images that are not available and uses previously built ones when possible.
  * Never: Don't build any images. Always use previously built images or throw an error if some image is not available. This is similar to using the `--no-build` option with the `docker compose up` command.
  * Always: Always build images before starting containers. This is similar to using the `--build` option with the `docker compose up` command.

  
Stop Containers| Configure how to stop containers in a service. By default, Docker Compose doesn't stop other containers in a service. You have to stop them manually.However, you can choose to stop all containers if any container in a service stops. This is similar to using the `--abort-on-container-exit` option with the `docker compose up` command.  
  
21 October 2025

[Dockerfile run configuration](dockerfile-run-configuration.html)[Docker run targets](docker-run-targets.html)
