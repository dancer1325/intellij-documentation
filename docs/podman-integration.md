[//]: # (Source: https://www.jetbrains.com/help/idea/podman-integration.html)
[//]: # (Downloaded: 2025-12-17 19:34:02)

# Start Dev Container with Podman

IntelliJ IDEA supports creating a Dev Container using [Podman](podman.html). Currently, this support is still in development.

Before you start creating a Dev Container, ensure that [Podman](https://podman-desktop.io/docs/installation) is configured and the minimal prerequisites for Dev Containers are met.

### Create a Dev Container with Podman

  1. Configure [Podman](podman.html).

  2. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Docker.

  3. Under the Podman section in the Podman connection list, ensure that you have a Podman machine up and running. Click OK. 

![Podman settings](https://resources.jetbrains.com/help/img/idea/2025.3/podman_settings.png)
  4. From the Welcome screen, select Remote Development and click Create Dev Container.

  5. On the page that opens, select the Podman configuration and select the [necessary project](start-dev-container-from-welcome-screen.html).

  6. Click Build Container and Continue. 

After the Dev Container is built, the project is opened with JetBrains Client.




28 October 2025

[Start Dev Container inside IDE](start-dev-container-inside-ide.html)[Recent Dev Containers](recent-dev-containers.html)
