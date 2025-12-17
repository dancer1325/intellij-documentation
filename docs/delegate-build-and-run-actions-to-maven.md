[//]: # (Source: https://www.jetbrains.com/help/idea/delegate-build-and-run-actions-to-maven.html)
[//]: # (Downloaded: 2025-12-17 19:24:33)

* IntelliJ IDEA 
  * lets you, about Maven projects
    * link,
    * ignore projects,
    * synchronize changes | Maven and IntelliJ IDEA projects,
    * configure the build and run actions

## Navigate to POM
* TODO:

## TODO:

## Link and unlink a Maven project

You can have multiple Maven projects inside one IntelliJ IDEA project. It might be helpful if you keep parts of code in different projects or have some legacy projects on which you need to work. You can link such projects in IntelliJ IDEA and manage them simultaneously. You can also quickly remove such projects from the Maven structure.

### Link a Maven project

  1. Open the [Maven](maven-projects-tool-window.html) tool window.

  2. In the Maven tool window, click ![the Link Maven Projects icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to attach a Maven project.

  3. In the dialog that opens, select the desired pom.xml file, and click OK. 

The project is linked. The Maven tool window shows the toolbar and a tree view of Maven entities.




### Unlink a Maven project

When you unlink a Maven project, IntelliJ IDEA removes all relevant projects and content roots, removes the Maven project from both the Maven tool window and the Project tool window, and stops its synchronization. It might be helpful if you need to fully remove the previously linked Maven project from the current IntelliJ IDEA project.

  1. In the [Maven](maven-projects-tool-window.html) tool window, right-click a linked project.

  2. From the context menu, select Unlink Maven Projects (`Delete`). Alternatively, you can select the linked project and click ![the Remove icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) on the tool window's toolbar.

  3. Click OK.





## TODO:

## Delegate build and run actions -- to -- Maven

* IntelliJ IDEA
  * 💡ways to build a Maven project💡
    * native IntelliJ IDEA builder
      * ⚠️default one⚠️  
      * use cases
        * pure Java OR Kotlin project
          * Reason:🧠IntelliJ IDEA speeds up the building process -- via -- the [incremental build](compiling-applications.md)🧠 
    * Maven
      * use cases
        * configuration / changes the compilation | fly
        * your build generates an artifact / custom layout

### Build a project -- with -- Maven
* steps
  * File > Settings > Build, Execution, Deployment > Build tools > Maven > Runner > Delegate IDE build / run actions to Maven
  * Build > Build project

### Run and debug -- with -- Maven
* steps
  * [PREVIOUS steps](#build-a-project----with----maven)
  * Run > Run, OR Run > Debug

* | debugging process,
  * [HotSwap](altering-the-program-s-execution-flow.md) is triggered
  * classes are reloaded