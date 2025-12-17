[//]: # (Source: https://www.jetbrains.com/help/idea/start-dev-container-for-a-remote-project.html)
[//]: # (Downloaded: 2025-12-17 20:03:17)

# Start Dev Container for a remote project

You can start a Dev Container on the remote machine for the project with the `.json` file located in the remote file system or for the project cloned from a Git repository.

Before you start creating a Dev Container on a remote machine, ensure you have Docker installed on the remote server. In addition, ensure you have Java version 17 or higher installed on the remote server if you want to build a Dev Container for a project located in the remote file system.

### Start Dev Container on a remote server

  1. Launch IntelliJ IDEA.

  2. From the welcome screen, click Remote Development, and from the options on the right, click Create Dev Containers. 

![Dev Containers](https://resources.jetbrains.com/help/img/idea/2025.3/idea_dev_container.png)
  3. On the page that opens, click ![Show option menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) to connect to Docker on a remote machine by SSH. 

![Docker](https://resources.jetbrains.com/help/img/idea/2025.3/docker_config.png)

If your remote server is not configured, click ![Show option menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) and on the page that opens [add the necessary options](settings-tools-ssh-configurations.html).

![SSH Configuration](https://resources.jetbrains.com/help/img/idea/2025.3/server_config.png)
  4. Select the IDE backend that you want to use for the project. 

If you want to change the selected IDE, click ![Show option menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) and select the one you need from the list.

  5. Select a project for which you want to build a Dev Container by clicking the appropriate tab:

The project to which you are referring should have a `devcontainer.json` file that contains the Dev Container configuration.

This option lets you choose a project residing on your remote machine.

Specify a path to the `.json` file of the project.

![JSON file from a remote file system](https://resources.jetbrains.com/help/img/idea/2025.3/from_remote_project_file.png)

This option lets you specify a project residing on GitHub. Specify the following options:

     * Git Repository: specify the path to your project on GitHub.

     * Automatic: select this option if you want IntelliJ IDEA to detect the `.json` file automatically.

     * Specify Path: select this option if you prefer to specify the path to the `.json` file manually.

![Git repository](https://resources.jetbrains.com/help/img/idea/2025.3/from_git_project.png)

Click Build Container and Continue.

  6. After the Dev Container is built, the project opens in the JetBrains Client.

At this point, you can work with your project further.




28 October 2025

[Customizing various Dev Container settings](customizing-devcontainer-json-file.html)[Start Dev Container from the IDE welcome screen](start-dev-container-from-welcome-screen.html)
