[//]: # (Source: https://www.jetbrains.com/help/idea/how-to-use-wsl-development-environment-in-product.html)
[//]: # (Downloaded: 2025-12-17 19:28:55)

## Use WSL to run a project in the Windows file system

You can [create](new-project-wizard.html) or [open](import-project-or-module-wizard.html) your project locally on Windows OS with local JDK and then run your compiled code in WSL using [run targets](run-targets.html). This might be helpful for the cross-platform development.

The run target feature is supported in the IntelliJ IDEA Ultimate edition only.

You might need to configure [firewall settings](#debugging_system_settings), before you use WSL features in the IDE.

### Create a run configuration for WSL

  1. In the main menu, click Run | Edit Configurations Alternatively, press `Alt+Shift+F10`, then `0`.

  2. Select one of the [supported](run-targets.html#supported-rcs) run/debug configuration types.

  3. From the Run on menu, under the New targets section, select WSL to add a WSL target.

When you add the WSL target, IntelliJ IDEA performs an introspection and automatically adds a path to a remote JDK in WSL, and the JDK version in the New Target: WSL dialog.

![New Target: WSL](https://resources.jetbrains.com/help/img/idea/2025.3/new_target_wsl.png)
  4. If you need to add additional information to the existing WSL target, click Manage targets and in the Run Targets dialog, add the needed information. For example, you can select Maven or Gradle as a runtime. Click OK to save the changes. 

![Run targets dialog](https://resources.jetbrains.com/help/img/idea/2025.3/run_target_dialog.png)
  5. In the main menu, go to Run and select the necessary run configuration or press (`Shift+F10`) to run your code and check the output in the Run tool window.



