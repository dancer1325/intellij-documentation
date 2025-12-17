[//]: # (Source: https://www.jetbrains.com/help/idea/settings-docker.html)
[//]: # (Downloaded: 2025-12-17 20:00:55)

## Virtual machine path mappings for Windows and macOS hosts

The Docker Engine runs natively on Linux. On Windows and macOS, Docker is executed in a lightweight Linux virtual machine, so containers can only access files that exist inside that VM.

The table below the Docker connection configuration options lets you configure the mapping between your local file system and the virtual machine running the Docker Engine, making them available for volume mounts in containers.

![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add `Alt+Insert`
    

Add a new mapping.

![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) Remove `Ctrl+Y`
    

Remove the selected mapping.

![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inline_edit.svg) Edit `Enter`
    

Edit the selected mapping.

Virtual machine path
    

The path to the directory in the virtual machine used for running this Docker Engine.

Local path
    

The path to the local folder that you want to map to the corresponding directory in the virtual machine. You will not be able to bind-mount anything outside of this folder to containers that this Docker Engine runs.

For example, let's say you keep all files that you bind-mount to Docker containers in /Users/jsmith/docker-share. You can map this directory to /dockerShare on the virtual machine for your Docker Engine connection. This Docker Engine will effectively bind-mount files to containers from /dockerShare, because that's where it can access the files that you mapped from /Users/jsmith/docker-share.

This does not affect you as a user running containers, because you still configure bind mounts and volumes as a mapping between some path on your host machine and some path inside the container. However, you can't mount anything outside of the directory that you mapped to the virtual machine.

Let's say you run a container and mount the directory with your application artifacts /Users/jsmith/docker-share/out on the host to /usr/local/tomcat/webapps in the container. In this case, the Docker Engine actually mounts /dockerShare/out, because that's where it has access to your files through virtual machine mapping.

![Path mapping for virtual machine running Docker Engine](https://resources.jetbrains.com/help/img/idea/2025.3/docker_path_mappings_for_vm.png)

For more information about volumes and bind mounts, refer to [Manage data in Docker](https://docs.docker.com/storage/).
