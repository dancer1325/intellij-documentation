[//]: # (Source: https://www.jetbrains.com/help/idea/maven-projects-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:32:09)

## Toolbar Buttons

Item| Description  
---|---  
![Reimport All Maven Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg)| Click this button to synchronize all Maven projects with the IntelliJ IDEA project. See [Importing tab](maven-importing.html) of the Maven Integration dialog.  
![Generate Sources and Update Folders for All Projects](https://resources.jetbrains.com/help/img/idea/2025.3/maven.images.expui.build.updateFolders.svg)| Click this button to launch Maven goals for generating sources and resources for the source and test directories, and read the resulting directory structure. According to the results of such generation, the IntelliJ IDEA folders are properly marked as the source or test roots.See [import settings](maven-importing.html).  
![Download Sources and/or Documentation](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.download.svg)| Click this button to download missing sources and documentation. Select the desired download option from the submenu.You can set up automatic downloading of sources and documentation at the [Importing](maven-importing.html) page of the Maven Integration dialog.  
![Add Maven Project](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)| Click this button to add a Maven project. Select the desired pom.xml file in the dialog that opens.  
![Run Maven Build](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg)| Click this button to execute the selected phase of the build lifecycle or a plugin goal. If several goals are selected, they will be executed in the same order as in the tree. Note that by default this button is disabled, to activate it you need to select a build phase or a plugin [goal](work-with-maven-goals.html) to run.  
![Execute Maven Goal](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.runAnything.svg)| Click this button to execute a maven goal using the [Run Anything](work-with-maven-goals.html#run_maven_command_line) window.  
![Toggle Offline Mode](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.build.toggleOfflineMode.svg)| Click this button to toggle the [offline mode](working-offline.html#maven).  
![Toggle Skip Test Mode](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.showIgnored.svg)| Click this button to turn on the Maven option [Skip test mode](work-with-tests-in-maven.html#skip_test), and omit running unit tests.  
![Analyze Dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.build.dependencyAnalyzer.svg)| Click this icon to open the [Dependency Analyzer](work-with-maven-dependencies.html#dependency_analyzer) window.  
![Show Dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.fileTypes.diagram.svg)| Click this button to show the dependencies of the current Maven project in a [UML frame](work-with-maven-dependencies.html#maven_dependency_diagram).  
![Collapse All](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.collapseAll.svg)| Click this button to collapse all nodes under the selected Maven project.  
![Build Tools Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg)| Use this icon to access the following settings:

  * Auto-Reload Setting: select this option to configure the reloading process of your Gradle project in the [Build Tools settings](settings-build-tools.html) dialog.
  * Maven Settings: select this option to configure the settings of the current Maven project in the [Maven settings](maven.html) dialog.

  
![Show Options Menu](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg)| Click this button to show the menu of the show options:

  * Group Modules: select this option to group the nodes by directories.
  * Show Ignored Projects :select this option to display the [ignored projects](delegate-build-and-run-actions-to-maven.html#ignore_maven_project) the tool window.In the Maven tool window, the ignored projects are greyed out.![Maven tool window: Ignored projects](https://resources.jetbrains.com/help/img/idea/2025.3/ignored_project_maven.png)
  * Show Basic Phases Only: when this option is selected, IntelliJ IDEA shows only the basic build phases; otherwise, the complete list of phases is shown.
  * Always Show ArtifactId: select this option to display the artifactId that is specified in the pom.xml of your Maven project.
  * Show version: when this option is selected, IntelliJ IDEA displays the version of your Maven project that is specified in the pom.xml.
  * Show Toolbar: by default, this option is selected and the Maven tool window displays a toolbar with different actions from which you can select. If you don't want to view the toolbar, unselect this option.
  * [Pinned Mode, Docked Mode, Floating Mode, Split Mode](project-tool-window.html#viewing_modes)
  * Group Tabs: deselect this option to see the views on separate tabs if more than one view is available in a tool window.
  * Move to: select this option to move the Maven Projects tool window to either top, left or right.
  * Resize: select this option to resize the Maven Projects tool window.


