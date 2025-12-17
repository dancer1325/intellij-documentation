[//]: # (Source: https://www.jetbrains.com/help/idea/docker-troubleshooting.html)
[//]: # (Downloaded: 2025-12-17 19:25:13)

# Docker troubleshooting

JetBrains is constantly working on fixes and improvements for the Docker plugin. You can find the [list of known Docker issues and feature requests](https://youtrack.jetbrains.com/issues?q=tag:docker-limitations) in our bug-tracking system and vote for the ones that affect you the most. You can also file your own bugs and feature requests.

If you encounter one of the following problems, try the corresponding suggested solution:

Can't connect to the Docker daemon from IntelliJ IDEA
    

Make sure that:

  * [Docker is installed and running](docker.html#install_docker)

  * [You correctly configured the Docker daemon connection in IntelliJ IDEA settings](docker.html#daemon-connection)




For more information, refer to [Docker connection settings](settings-docker.html).

Can't run a multi-container application with Docker Compose
    

Make sure that the Docker Compose executable is specified correctly in the Settings dialog `Ctrl+Alt+S` under Build, Execution, Deployment | Docker | Tools. For more information, refer to [Docker connection settings](settings-docker.html).

Docker Compose doesn't work on Ubuntu via Unix socket settings
    

When running Docker Compose on Ubuntu, you see the following error message:

docker.errors.TLSParameterError: Path to a certificate and key files must be provided through the client_config param. TLS configurations should map the Docker CLI client configurations. 

In this case, use TCP socket connection with `unix:///var/run/docker.sock` in the Engine API URL field. For more information, refer to [TCP socket](settings-docker.html#tcp_socket).

Can't use port bindings
    

Make sure that the corresponding container ports are exposed. Use the [EXPOSE](https://docs.docker.com/engine/reference/builder/#expose) command in your [Dockerfile](https://docs.docker.com/engine/reference/builder/).

Can't pull an image from a registry
    

When you try to pull a Docker image from a registry, the following message is displayed:

Failed to parse dockerCfgFile: <your_home_dir>/.docker/config.json, caused by: ... {"credsStore":"wincred"} 

In this case, go to the <your_home_dir>/.docker directory and delete the config.json file.

Can't associate Dockerfile and Docker Compose files with proper types
    

By default, IntelliJ IDEA should be able to identify Dockerfile and Docker Compose files by their names and contents. This enables various coding assistance features for those files, such as completion suggestions, inspections, and gutter icons. If IntelliJ IDEA doesn't recognize a file, it prompts you to specify the file type manually. To associate an existing file with the correct type, right-click it in the Project tool window and select Associate with File Type from the context menu.

If the Associate with File Type action is disabled, this probably means that the filename is registered as a pattern for some other file type. For example, if you have a Dockerfile with a custom name that is recognized as a text file, you cannot associate it with the Dockerfile type. To remove the file type pattern, do the following:

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | File Types.

  2. Select the relevant file type (in this case: Text) and remove the pattern with the name of the file.

  3. Click OK to apply the changes.




Now you should be able to set the correct file type using Associate with File Type in the context menu.

High CPU usage while connecting to Docker via services
    

If you are using Hyper-V as the backend for the Docker service on Windows, antivirus software will constantly scan Hyper-V virtual disk files (.vhdx), This causes excessive consumption of CPU resources, even if there are no containers running.

In this case, exclude Hyper-V virtual disk files from the antivirus scan.

09 April 2025

[Deploy and debug a Java web application inside a container running Tomcat](docker-tutorial-tomcat-debug.html)[Podman](podman.html)
