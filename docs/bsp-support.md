[//]: # (Source: https://www.jetbrains.com/help/idea/bsp-support.html)
[//]: # (Downloaded: 2025-12-17 19:19:30)

# BSP support

The Build Server Protocol (BSP) defines a standard way for the build tool such as [sbt](sbt-support.html) or [Mill](http://www.lihaoyi.com/mill/) to interact with IDEs, letting you import your project, run compilation and other tasks, get error messages and progress updates directly in the IDE.

The Scala plugin for IntelliJ IDEA supports BSP as a client.

### Open an sbt project from the BSP model

  1. On the welcome screen, press `Ctrl+Shift+A` and search for the Project from Existing Sources action. 

Alternatively, go to File | New | Project from Existing Sources in the main menu.

If you already have an existing sbt project, you can follow the same [procedure](#import_bsp) to convert your project to a BSP one.

  2. In the dialog that opens, select a directory that contains your sbt project.

  3. On the page that opens, select the BSP option and click Next. 

![The BSP import model](https://resources.jetbrains.com/help/img/idea/2025.3/bsp_model.png)
  4. Click Finish. 

IntelliJ IDEA opens the project, configures the BSP server, and loads all the necessary dependencies. The BSP tool window displays the imported project and its dependencies.

![BSP downloaded project](https://resources.jetbrains.com/help/img/idea/2025.3/bsp_download_project.png)

On the status bar there is the BSP Connection icon that you can click and disable the connection either just one project or for all BSP connections.




If you come across problems with importing a BSP project, check whether you have the latest version of the sbt, Bloop, or Mill server downloaded.

26 May 2024

[Separate main and test modules in sbt](sbt-separate-modules.html)[Akka support](akka-support.html)
