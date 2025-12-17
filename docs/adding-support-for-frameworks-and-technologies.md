[//]: # (Source: https://www.jetbrains.com/help/idea/adding-support-for-frameworks-and-technologies.html)
[//]: # (Downloaded: 2025-12-17 19:17:55)

# Add frameworks (facets)

This information is valid for projects that are built with the native IntelliJ IDEA builder. If you're using a build tool, such as [Maven](maven-support.html) or [Gradle](gradle.html), make all changes using the build file.

For developing framework-specific applications, IntelliJ IDEA features facets. Facets contain libraries, dependencies, and technologies, and they provide you with additional UI elements for configuring framework-specific settings.

Note that not all facets are available out of the box. To be able to use some of them, you need to install a plugin for the necessary framework first. For more information about existing plugins, refer to [JetBrains Marketplace](https://plugins.jetbrains.com/).

IntelliJ IDEA can identify a file or a directory that is typical for a certain framework and add the necessary facet for you. Once the facet is detected and added, IntelliJ IDEA will inform you about the missing configuration and will suggest the necessary actions.

If a facet is not detected automatically, you can [add it manually](#manually-add-facet-to-module). You can add more than one facet to a module.

Some frameworks are available only with the Ultimate subscription. Refer to [comparison matrix](https://www.jetbrains.com/idea/features/editions_comparison_matrix.html) to make sure your IntelliJ IDEA supports the necessary frameworks.

You can find all facets that are configured for modules in your project in the Project Structure dialog: in the main menu, go to File | Project Structure (`Ctrl+Alt+Shift+S`) and select Modules.

If you use a build tool in your project, such as [Maven](maven-support.html) or [Gradle](gradle.html), make all changes using the build file.

![Facets configured for modules in Project Structure dialog](https://resources.jetbrains.com/help/img/idea/2025.3/facets-in-modules.png)

### Manually add a facet to a module

  1. Press `Alt+1` or go to View | Tool Windows | Project in the main menu to open the Project tool window.

  2. In the Project tool window, select the module to which you want to add a facet.

  3. Press `Ctrl+Shift+A` and type `Add Framework Support`.

Once the action is found, click it to open the Add Framework Support dialog.

  4. Select the necessary framework from the list.

Depending on your choice, you might be prompted to configure additional settings (for example, to configure a library).

  5. Apply the changes and close the dialog.


![Adding a new facet manually](https://resources.jetbrains.com/help/img/idea/2025.3/framework_support_dialog.png)

### Disable framework auto-detection

By default, auto-detection is enabled for all the supported frameworks. You can disable framework auto-detection completely, or exclude individual frameworks from auto-detection.

  1. In the main menu, go to File | Project Structure (`Ctrl+Alt+Shift+S`) and select Facets.

  2. Select Detection and click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) `Alt+Insert`.

  3. From the Framework to Exclude list, select the necessary option.

You can disable auto-detection of a specific framework only in one directory or in the whole project. The list also allows you to disable auto-detection of all frameworks in a specific directory.

  4. If you want to disable auto-detection of all frameworks in the whole project, deselect the Enable framework detection checkbox.

To re-enable auto-detection everywhere, select the Enable framework detection checkbox and remove all entries from the Exclude from detection list.


![Excluding a framework from auto-detection](https://resources.jetbrains.com/help/img/idea/2025.3/framework-detection.png)

In this dialog, you can also remove a framework or add a new one.

18 November 2025

[Module dependencies](working-with-module-dependencies.html)[Unload modules](unloading-modules.html)
