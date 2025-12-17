[//]: # (Source: https://www.jetbrains.com/help/idea/sbt-separate-modules.html)
[//]: # (Downloaded: 2025-12-17 19:59:40)

# Separate main and test modules in sbt

There is a new, experimental mode of working with sbt projects in IntelliJ IDEA with the Scala plugin. If enabled, it organizes main and test sources into separate modules, which improves compilation and dependency management.

### Enable the separate modules mode

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Build Tools | sbt.

  2. Enable the Create separate modules for main and test sources option.

![Create separate modules for main and test sources](https://resources.jetbrains.com/help/img/idea/2025.3/sbt_create_separate_modules.png)
  3. Click OK. The project will be reloaded automatically, and new modules will be created.

  4. After the reload, each run configuration referencing a module should switch to the corresponding main or test module. In rare cases, changing the modules in the run configurations may not be possible automatically.

If this happens, you can update the run configurations by explicitly using the Update Run Configurations to a new module naming scheme action. You can find it using Find Action `Ctrl+Shift+A` or by navigating to Tools | Scala in the main menu.

![Update Run Configurations to the new module naming scheme](https://resources.jetbrains.com/help/img/idea/2025.3/sbt_update_run_configuration.png)



Refer to the [New Module Layout for sbt Projects](https://blog.jetbrains.com/scala/2024/11/19/new-module-layout-for-sbt/) article in the JetBrains blog for more details and examples of how this new mode helps configure sbt projects.

09 July 2025

[sbt](sbt-support.html)[BSP support](bsp-support.html)
