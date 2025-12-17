[//]: # (Source: https://www.jetbrains.com/help/idea/start-dev-container-from-scratch.html)
[//]: # (Downloaded: 2025-12-17 20:03:18)

# Start Dev Container from scratch

You can create a new Dev Container using a `devcontainer.json` file and the [configuration](https://containers.dev/implementors/json_reference/) options it offers.

The easiest way to start is to pull an image (a predefined template) for your `devcontainer.json` file from a container registry (the collection of repositories with the predefined images).

### Create a Dev Container

  1. Open a project in IntelliJ IDEA.

  2. In the [Project](creating-and-managing-projects.html) view, right-click the name of your project and select New | Dev Container Config.

  3. In the dialog that opens, IntelliJ IDEA displays a default container configuration. If you want, you can select other Dev Container templates from the Dev Container Template list. 

![Create a new Dev Container](https://resources.jetbrains.com/help/img/idea/2025.3/create_new_dev_container.png)
  4. Click OK. 

IntelliJ IDEA generates the .devcontainer directory with the devcontainer.json file that contains the container description. You can customize the configuration as needed.

![Dev Container result](https://resources.jetbrains.com/help/img/idea/2025.3/create_dev_container_result.png)
  5. In the left gutter, click ![Create Dev Container](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-docker-gateway.icons.devContainers.svg) and select Create Dev Container and Mount Sources to build your Dev Container.




07 August 2025

[Start Dev Container from the IDE welcome screen](start-dev-container-from-welcome-screen.html)[Start Dev Container inside IDE](start-dev-container-inside-ide.html)
