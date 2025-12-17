[//]: # (Source: https://www.jetbrains.com/help/idea/remote-development-overview.html)
[//]: # (Downloaded: 2025-12-17 19:57:10)

## Connections

The remote host is a physical or virtual machine hosting the source code and running a backend IDE. You connect to the backend that transparently provides full access to all IDE features.

A connection to the remote machine can be established using various scenarios:

### SSH connection

SSH connection from a local machine into a remote server or vice versa (from an already installed IDE on your server to your local machine).

You can use one of the following ways:

  * JetBrains Toolbox App: supports the connection on Linux, macOS, and Windows. For more information, refer to the [Toolbox App](https://www.jetbrains.com/help/toolbox-app/about-the-instance.html) page.

  * IntelliJ IDEA: connects to your remote project from the IntelliJ IDEA welcome screen. For more information, refer to [Connect to a remote server from IntelliJ IDEA](remote-development-starting-page.html).

  * JetBrains Gateway: you can use JetBrains Gateway for the SSH connection to a Linux machine. You can also connect to various development environments. 

For more information, refer to [Connect and work with JetBrains Gateway](remote-development-a.html).




### Dev Container connection

Development Container connection when starting a Dev Container on the remote machine for the project with the JSON file located in the remote file system or for the project cloned from a Git repository.

Refer to [Start Dev Container for a remote project](start-dev-container-for-a-remote-project.html) for this workflow description.

### WSL connection

WSL connection when configuring your IDE backend to launch directly in WSL2. JetBrains Gateway offers native WSL support for such a scenario.

Refer to [Connect to a project running on WSL2](remote-development-a.html#run_in_wsl) for more information.

### Dev Environments

Connections to various development environments running on JetBrains CodeCanvas, Gitpod, Google Cloud, GitHub Codespaces, Amazon CodeCatalyst, and Coder are also available through JetBrains Gateway.

For more information on how to connect to each of the environments, refer to [Connect and work with JetBrains Gateway](remote-development-a.html).
