[//]: # (Source: https://www.jetbrains.com/help/idea/services-tool-window.html)
[//]: # (Downloaded: 2025-12-17 20:00:10)

## Run/debug configurations

[Run/debug configurations](run-debug-configuration.html) are not listed in the Services tool window by default. You need to explicitly specify the types of configurations you want to be available and create the corresponding configurations.

### Add Run/Debug configurations to the Services window

  1. Select View | Tool Windows | Services from the main menu or press `Alt+8`.

  2. In the Services tool window, click Add service, then select Run Configuration Type.

![Services tool window: Add run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/services-add-rc.png)
  3. Select a run/debug configuration type from the list to add all configurations of this type to the window.

Note that the tool window will only display the configuration types for which you have [created](run-debug-configuration.html#create-permanent) one or more configurations.




Buttons on the toolbar depend on the selected type of the run/debug configuration and can include the following:

![The Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg)
    

Run `Ctrl+Shift+F10`

Run the selected configuration.

![The Debug button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.debug.svg)
    

Debug `⌃ ⇧ D`

Run the selected configuration in Debug mode.

![The Stop button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.stop.svg)
    

Stop `Ctrl+F2`

Stop the selected configuration.

![The Rerun button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.rerun.svg)
    

Rerun `Ctrl+Shift+F10`

Rerun the selected configuration.

![The Rerun in Debug Mode button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.restartDebug.svg)
    

Rerun in Debug Mode `⌃ ⇧ D`

Rerun the selected configuration in Debug mode.

![The Filters menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.show.svg)
    

Filters

Filter the output for the selected configuration. For example, you can select to show warnings and successful steps.

![The More menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg)
    

More

Additional actions related to the configuration. For example, you can open and modify the settings of the selected configuration.
