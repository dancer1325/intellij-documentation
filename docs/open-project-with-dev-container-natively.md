[//]: # (Source: https://www.jetbrains.com/help/idea/open-project-with-dev-container-natively.html)
[//]: # (Downloaded: 2025-12-17 19:33:27)

# Open a project with Dev Container natively

Starting with IntelliJ IDEA version 2025.3, you can open a Dev Container project in the same window where the Dev Container was built. This feature is still in development and may change in the future.

Before you start, note the following limitations:

  * This feature is not supported in the IntelliJ IDEA versions earlier than 2025.3.

  * Only Docker-based Dev Containers are supported.

  * The scenario of starting a Dev Container for a remote project is not supported.




### Enable Dev Container settings

  1. Press `Ctrl+Alt+S` to open settings and then select Advanced Settings.

  2. From the options on the right, under the Dev Containers section, select Open devcontainer projects natively.

  3. Click OK to save the changes.

  4. Use one of the [available scenarios](connect-to-devcontainer.html#dev_container_scenarios) to start a Dev Container and open your project. The project will be opened without connecting to a backend and additional client windows.




03 November 2025

[Dev Container CLI](dev-container-cli.html)[Integrated tools](integrated-tools.html)
