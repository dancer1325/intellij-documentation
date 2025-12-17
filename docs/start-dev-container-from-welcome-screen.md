[//]: # (Source: https://www.jetbrains.com/help/idea/start-dev-container-from-welcome-screen.html)
[//]: # (Downloaded: 2025-12-17 20:03:20)

# Start Dev Container from the IDE welcome screen

You can start a Dev Container from the IDE welcome screen to clone a project right into a Dev Container, or to open one from your local file system.

### Start Dev Container from Welcome Screen

  1. On the IDE Welcome Screen, click the Remote Development node.

  2. From the available options on the right, click Create Dev Container.

  3. On the page that opens, the connection to the local Docker is found automatically.

If there is no connection, check whether your local Docker is active.

  4. Specify the name of the backend IDE that will be used for the Dev Container. 

By default, it is the IDE that you currently use. If you want to change the selected IDE, click ![Show option menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) and select the one you need from the list.

  5. Select which project you want to use either from the VCS or from the local file system and fill out the necessary fields. 

     * Path to devcontainer.json: specify a path to the project's devcontainer.json file that you want to open from your local machine. 

![Local project Dev Container](https://resources.jetbrains.com/help/img/idea/2025.3/local_devcontainer_json.png)

     * Git Repository: In this field, specify the path to your project on GitHub. 

The project to which you are referring should have a `devcontainer.json` file that contains the Dev Container configuration.

Ensure that you have a running SSH agent on your local machine. For more information see [Prerequisites](prerequisites-for-dev-containers.html#ssh_agent).

     * Detection for devcontainer.json file: select whether you want to specify the path to a `devcontainer.json` file manually or let it be detected automatically.

![From VCS Project](https://resources.jetbrains.com/help/img/idea/2025.3/from_git_project.png)

Click Build Container and Continue.

  6. After the Dev Container is built, the project is opened with JetBrains Client.




28 October 2025

[Start Dev Container for a remote project](start-dev-container-for-a-remote-project.html)[Start Dev Container from scratch](start-dev-container-from-scratch.html)
