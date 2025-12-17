[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration.html)
[//]: # (Downloaded: 2025-12-17 19:59:01)

## Create permanent run/debug configurations

IntelliJ IDEA provides the following ways to create a permanent run/debug configuration:

  * When there is an executable class or method, you can [create a permanent run/debug configuration right from the editor](#from-class).

  * [Save a temporary run/debug configuration as permanent](#save-as-permanent).

  * [Create from a template](#createExplicitly) or copy an existing configuration.




### Create a permanent run/debug configuration from an executable method or class

  1. Place the caret at the declaration of an executable method or class (for example, a class with the `main()` method or a test suite) and press `Alt+Enter`.

  2. From the menu that opens, select Modify Run Configuration.

IntelliJ IDEA creates a permanent run/debug configuration of the corresponding type and opens a dialog in which you can set configuration parameters.

![Create run configuration for a class](https://resources.jetbrains.com/help/img/idea/2025.3/ij_create_rc_for_class.png)
  3. Set up the run/debug configuration parameters. For the detailed description of the template, see [List of run/debug configurations](list-of-run-debug-configurations.html).




### Save a temporary configuration as permanent

  * Select a temporary configuration in the [run widget](guided-tour-around-the-user-interface.html#toolbar), click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.actions.more.svg) and select Save Configuration.

![Save a temporary run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/save_temporary.png)
  * Alternatively, select a temporary configuration in the Run/debug configurations dialog and click ![Save](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.save.svg) on the toolbar.




IntelliJ IDEA provides run/debug configuration [templates](#templates) for different languages, tools, and frameworks. The list of available templates varies depending on the installed and enabled [plugins](managing-plugins.html).

### Create a run/debug configuration from a template

  1. Go to Run | Edit Configurations. Alternatively, press `Alt+Shift+F10`, then `0`. 

  2. In the Run/Debug Configurations dialog, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar or press `Alt+Insert`. The list shows the run/debug configuration templates. Select a template, for example, Application. This configuration compiles and runs your Java program – similar to when you use the `javac` and `java` commands. 

![Selecting a new run/debug configuration template](https://resources.jetbrains.com/help/img/idea/2025.3/ij-select-new-run-config.png)
  3. Specify the run/debug configuration name in the Name field. This name will be used to identify the run/debug configuration in lists and menus. 

  4. Specify the configuration options.

For more information, refer to [Run/debug configuration: Application](run-debug-configuration-java-application.html) (to run a simple Java application) or [List of run/debug configuration templates](list-of-run-debug-configurations.html) (for other run configurations).

  5. You can either run the configuration right away or save the configuration to run it later.

     * To save the run configuration for later, click OK.

     * To run the configuration right away, click Run.



