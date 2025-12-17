[//]: # (Source: https://www.jetbrains.com/help/idea/managing-plugins.html)
[//]: # (Downloaded: 2025-12-17 19:31:53)

## Required plugins

A project may require plugins that provide support for certain technologies or frameworks. You can add such plugins to the list of required plugins for the current project, so that IntelliJ IDEA will verify that the plugins are installed and enabled. It will notify you if you forget about some plugin, or someone on your team is not aware about the dependency as they work on the project. 

### Add a required plugin for your current project

Make sure the required plugin is installed.

  1. Press `Ctrl+Alt+S` to open settings and then select Appearance & Behavior | Required Plugins.

  2. On the Required Plugins page, click ![The Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the plugin. Optionally, specify the minimum and maximum version of the plugin.




To specify the required version of IntelliJ IDEA itself, add IDE Core to the list of required plugins.

The list of required plugins is stored in the .idea/externalDependencies.xml file of your project. When you open the project in IntelliJ IDEA, it will notify you if the required plugin is disabled, not installed, or requires an update.

Click the link in the notification message to quickly enable, install, or update the required plugin.
