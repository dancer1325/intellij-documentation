[//]: # (Source: https://www.jetbrains.com/help/idea/exporting-an-intellij-idea-project-to-eclipse.html)
[//]: # (Downloaded: 2025-12-17 19:26:06)

# Export an IntelliJ IDEA project to Eclipse

Before you start exporting a project, make sure that the Eclipse Integration plugin is [enabled](managing-plugins.html).

At present, migration from IntelliJ IDEA to Eclipse is subject to certain limitations:

  * IntelliJ IDEA modules with multiple content roots cannot not be migrated.

  * External sources in Eclipse are not migrated.

  * Only Java modules are created automatically during the export. However, any module can be converted to the Eclipse compatible format manually.

  * The default workspace JRE is not converted to/from the project SDK.




### Export a project to Eclipse

When you export an IntelliJ IDEA project to Eclipse, it results in creating Eclipse project files .project and .classpath for each module file .iml in the module directory that contains the content root.

  1. In the main menu, go to File | Export | Project to Eclipse.

The Export to Eclipse dialog displays the list of modules that have not been converted and switched to use the Eclipse format yet (the modules that have the IntelliJ IDEA module format .iml).

![Exporting a project to Eclipse](https://resources.jetbrains.com/help/img/idea/2025.3/export-to-eclipse.png)
  2. Select the modules you want to export.

  3. Select the suggested options if necessary:

     * Convert selected modules into Eclipse-compatible format: convert the modules selected in the Modules to export to the Eclipse-compatible format.

     * Export non-module libraries: IntelliJ IDEA creates a User Library configuration file for Eclipse *.userlibraries, containing definitions of all external libraries used in the project.

     * Path to resulting .userlibraries: the path to the generated *.userlibraries file. This field is available when the Export non-module libraries option is selected.

  4. Click OK.

The project is exported to the same directory. The Project tool window displays the newly created Eclipse files.

![The project is exported to Eclipse](https://resources.jetbrains.com/help/img/idea/2025.3/export-to-eclipse-result.png)



### Convert a module to the Eclipse-compatible format

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S`.

  2. Select the module you want to convert and switch to the Dependencies tab.

  3. From the Dependencies storage format list, select Eclipse (.classpath).

  4. Apply the changes and close the dialog. 


![Converting a module to Eclipse](https://resources.jetbrains.com/help/img/idea/2025.3/convert-module-to-eclipse.png)

26 March 2025

[Import a project from Eclipse](import-project-from-eclipse-page-1.html)[Migrate from NetBeans to IntelliJ IDEA](netbeans.html)
