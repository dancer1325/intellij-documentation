[//]: # (Source: https://www.jetbrains.com/help/idea/docker-containers.html)
[//]: # (Downloaded: 2025-12-17 19:25:07)

## Interacting with containers

Created containers are listed in the [Services](services-tool-window.html#docker) tool window. By default, the Services tool window displays all containers, including those that are not running. To hide stopped containers from the list, click ![The View Options button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) in the toolbar, select Docker, and then click Stopped Containers to remove the checkbox.

![Services tool window - Docker - filter](https://resources.jetbrains.com/help/img/idea/2025.3/services_tool_window_docker_filter.png)

When you select a container, you can view the Build Log tab that shows the deployment log produced by the corresponding [Docker run configuration](docker-run-configurations.html) while creating and starting the container.

![The Build Log tab of a container selected in the Services tool window](https://resources.jetbrains.com/help/img/idea/2025.3/docker-container-build-log-tab.png)

The Dashboard tab provides important information about the container. Besides its name and hash ID, it also lists the environment variables, ports, and volume bindings. You can add, edit, and remove the environment variables, ports, and volume bindings. However, these changes require you to recreate the container and do not change in the [Docker run configuration](docker-run-configurations.html) that is used to create this container. This means that the changes will not persist when you run the configuration next time.

![The Dashboard tab of a container selected in the Services tool window](https://resources.jetbrains.com/help/img/idea/2025.3/docker-container-dashboard.png)

For more information, refer to [Container dashboard](services-tool-window.html#docker-container-dashboard).

### Execute a command inside a running container

  1. In the Services tool window, right-click the container name and then click Exec.

  2. In the Run Command in Container popup, click Create and Run to create and execute a new command.

Alternatively, you can select one of the commands that you ran previously.

  3. In the Exec dialog, type the command and click OK. For example:

`ls /tmp`| List the contents of the /tmp directory  
---|---  
`mkdir /tmp/my-new-dir`| Create the my-new-dir directory inside the /tmp directory  
`/bin/bash`| Start a `bash` session  
  
![The Exec tab with /bin/bash running](https://resources.jetbrains.com/help/img/idea/2025.3/67_DockerExecBinBash_1.png)



For more information, refer to the [docker exec](https://docs.docker.com/engine/reference/commandline/exec/) command reference.

### View detailed information about a running container

  * In the Services tool window, right-click the container name and then click Inspect.

The output is rendered as a JSON object on the Inspection tab.

![The Inspection tab](https://resources.jetbrains.com/help/img/idea/2025.3/68_DockerInspect.png)



For more information, refer to the [docker inspect](https://docs.docker.com/engine/reference/commandline/inspect/) command reference.

### View processes running in a container

  * In the Services tool window, right-click the container name and then click Show Processes.

The output is rendered as a JSON array on the Processes tab.




For more information, refer to the [docker top](https://docs.docker.com/engine/reference/commandline/top/) command reference.

### Attach a console to the container output

  * In the Services tool window, right-click the container and then click Attach.

The console is attached to the output of the [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#entrypoint) process running inside a container, and is rendered on the Attached Console tab.




For more information, refer to the [docker attach](https://docs.docker.com/engine/reference/commandline/attach/) command reference.

### Browse files in a container

  1. In the Services tool window, right-click the container and then click Show Files.

  2. IntelliJ IDEA [executes](#execute-command) the `ls` command in the container and opens the Files tab with the container's file system.




On the Files tab, you can double-click any file to view it in the editor. IntelliJ IDEA opens the file in read-only mode, so you cannot edit or delete it.

Browsing files does not work for containers without the full `ls` package (for example, images that are based on Alpine, Photon, and BusyBox). For such containers, add the corresponding command in the Dockerfile, so the image installs the necessary package, for example:

FROM alpine:3.10 RUN apk add coreutils 

FROM photon:3.0 RUN echo y | tdnf remove toybox 
