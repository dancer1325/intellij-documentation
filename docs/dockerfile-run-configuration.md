[//]: # (Source: https://www.jetbrains.com/help/idea/dockerfile-run-configuration.html)
[//]: # (Downloaded: 2025-12-17 19:25:17)

# Dockerfile run configuration

Use this type of configuration to build an image from a Dockerfile and then derive a container from this image.

![Dockerfile run configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/dockerfile-run-config.png)

Docker uses the [docker build](https://docs.docker.com/engine/reference/commandline/build/) command to build an image from a Dockerfile, and then the [docker run](https://docs.docker.com/engine/reference/commandline/run/) command to start a container from it.

By default, the Dockerfile configuration has the following options:

Item| Description  
---|---  
Name| Specify a name for the run configuration to quickly identify it among others when editing or running.  
Allow multiple instances| Allow running multiple instances of this run configuration in parallel.By default, it is disabled, and when you start this configuration while another instance is still running, IntelliJ IDEA suggests stopping the running instance and starting another one. This is helpful when a run configuration consumes a lot of resources and there is no good reason to run multiple instances.  
Store as project file| Save the file with the run configuration settings to share it with other team members. The default location is .idea/runConfigurations. However, if you do not want to share the .idea directory, you can save the configuration to any other directory within the project.By default, it is disabled, and IntelliJ IDEA stores run configuration settings in .idea/workspace.xml.  
Server| Select the [Docker daemon connection](docker.html#connect_to_docker) to use for the run configuration.  
Dockerfile| Specify the name and location of the Dockerfile used to build the image.  
Image tag| Specify an optional name and tag for the built image.This can be helpful for referring to the image in the future. If you leave the field blank, the image will have only a random unique identifier.  
Container name| Specify an optional name for the container. If empty, Docker will generate a random name for the container.This is similar to using the `--name` option with the `docker run` command.  
Before launch| Specify a list of tasks to perform before starting the run configuration. For example, run another configuration, build the necessary artifacts, run some external tool or a web browser, and so on.Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or press `Alt+Insert` to add one of the available tasks.Move tasks in the list using ![the Up button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg) and ![the Down button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg) to change the order in which to perform the tasks. Select a task and click ![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) to edit the task. Click ![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) to remove the selected task from the list.  
Show this page| Show the run configuration settings before actually starting it.  
Activate tool window| Depending on the type of configuration, open the [Run](run-tool-window.html), [Debug](debug-tool-window.html), or [Services](services-tool-window.html) tool window when you start this run configuration. If this option is disabled, you can open the tool window manually:

  * View | Tool Windows | Run or `Alt+4`
  * View | Tool Windows | Debug or `Alt+5`
  * View | Tool Windows | Services or `Alt+8`

  
  
Use the Modify options menu to add advanced options to the run configuration:

Item| Description  
---|---  
Context folder| Specify a local directory that the daemon will use during the build process. All host paths in the Dockerfile will be processed relative to this directory. By default, if you leave it blank, Docker uses the same directory where the Dockerfile is located.  
Build args| Specify the values for build-time variables that can be accessed like regular environment variables during the build process but do not persist in the intermediate or final images.This is similar to using the `--build-args` option with the `docker build` command.These variables must be defined in the Dockerfile with the `ARG` instruction. For example, you can define a variable for the version of the base image that you are going to use: ARG PGTAG=latest FROM postgres:$PGTAG  The `PGTAG` variable in this case will default to `latest` and the Dockerfile will produce an image with the latest available version of PostgreSQL, unless you redefine it as a build-time argument. If you set, `PGTAG=9`, Docker will pull `postgres:9` instead, which will run a container with PostgreSQL version 9.Redefining the `PGTAG` argument is similar to setting the following command-line option:\--build-arg PGTAG=9You can provide several arguments separated by spaces.  
Build options| Set supported [`docker build` options](https://docs.docker.com/engine/reference/commandline/build/#options).For example, you can specify metadata for the built image with the `--label` option.  
Run built image| If selected, IntelliJ IDEA will run a Docker image after building it.  
Randomly publish all exposed ports| Publish all exposed container ports to random free ports on the host.This is similar to using the `-P` or `--publish-all` option on the command line.  
Bind ports| Map specific container ports to specific ports on the host.This is similar to using the `-p` or `--publish` option on the command line.Click ![Browse](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) in the Bind ports field and specify which ports on the host should be mapped to which ports in the container. You can also provide a specific host IP from which the port should be accessible (for example, you can set it to `127.0.0.1` to make it accessible only locally, or set it to `0.0.0.0` to open it for all computers in your network).Lets say you already have PostgreSQL running on the host port 5432, and you want to run another instance of PostgreSQL in a container and access it from the host via port 5433. Binding the host port 5433 to port 5432 in the container is similar to setting the following command-line option:-p 5433:5432You can set this option explicitly in the Run options field instead of configuring the Bind ports field.  
Entrypoint| Override the default `ENTRYPOINT` of the image.This is similar to using the `--entrypoint` option on the command line.  
Command| Override the default `CMD` of the image.This is similar to adding the command as an argument for `docker run`.  
Bind mounts| Mount files and directories on the host to a specific location in the container.This is similar to using the `-v` or `--volume` option on the command line.Make sure that the necessary local paths are mapped to the virtual machine in the [Docker connection settings](docker.html#daemon-connection) (the Path mappings table).Click ![Browse](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) in the Bind mounts field and specify the host directory and the corresponding path in the container where it should be mounted. Select Read only if you want to disable writing to the container volume.For example, you can mount a local PostgreSQL directory on the host (/Users/Shared/pg-data) to some directory inside the container (/var/lib/pgsql/data). Mounting volumes in this manner is similar to setting the following command-line option:-v /Users/Shared/pg-data:/var/lib/pgsql/dataYou can set this option explicitly in the Run options field instead of configuring the Bind mounts field.  
Environment variables| Specify environment variables. There are environment variables associated with the base image that you are using as defined by the `ENV` instruction in the [Dockerfile](https://docs.docker.com/engine/reference/builder/). There are also [environment variables that Docker sets automatically](https://docs.docker.com/engine/reference/run/#env-environment-variables) for each new container. Use this field to override any of the variables or specify additional ones.This is similar to using the `-e` or `--env` option on the command line.Click ![Browse](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) in the Environment variables field to add names and values for variables. For example, if you want to connect to PostgreSQL with a specific username by default (instead of the operating system name of the user running the application), you can set the `PGUSER` variable to the necessary value. This is similar to setting the following command-line option:\--env PGUSER=%env-var-valueYou can set this option explicitly in the Run options field instead of configuring the Environment variables field.  
Run options| Set any other supported [docker run](https://docs.docker.com/engine/reference/commandline/run/) options.For example, to connect the container to the `my-net` network and set the `my-app` alias for it, specify the following:\--network my-net --network-alias my-appNot all `docker run` options are supported. If you would like to request support for some option, leave a comment in [IDEA-181088](https://youtrack.jetbrains.com/issue/IDEA-181088).  
Attach to container| Attach to the container's standard input, output, and error streams.This is similar to using the `-a` or `--attach` option on the command line.  
Show command preview| Preview the resulting command that will be used to execute the run configuration.  
  
08 October 2024

[Docker Image run configuration](docker-image-run-configuration.html)[Docker compose run configuration](docker-compose-run-configuration.html)
