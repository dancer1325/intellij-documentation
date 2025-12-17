[//]: # (Source: https://www.jetbrains.com/help/idea/bazel.html)
[//]: # (Downloaded: 2025-12-17 19:18:42)

## Open a project

### Open a Bazel project

  1. Click Open on the Welcome screen.

Alternatively, go to File | Open in the main menu.

  2. In the dialog that opens, specify the path to the project sources.




You can watch the process of importing the project in the Build tool window:

![The Build tool window in the process of a Bazel project sync](https://resources.jetbrains.com/help/img/idea/2025.3/bazel-sync-build-tool.png)

Opening a Bazel project directory will create a default project view file projectview .bazelproject that loads the whole workspace.

### Open a project subset

Since Bazel is commonly used for large-scale projects, you may want to open a project subset to ease the load on the IDE. The Bazel plugin generally supports the project view files feature [as implemented by Google](https://ij.bazel.build/docs/project-views.html).

  * In the Project tool window (`Alt+1` or View | Tool Windows | Project in the main menu), right-click the predefined project view file and select Load Project View. 

![The Project tool window with a context menu for a .bazelproject file](https://resources.jetbrains.com/help/img/idea/2025.3/bazel-load-project-view.png)
  * Alternatively, click Open on the Welcome screen or go to File | Open in the main menu and select the predefined project view file.




### Resync project on file changes

When you change BUILD, WORKSPACE, MODULE.bazel or other build definition files, the IDE shows a popup with the button to update the loaded project structure. Click this icon to reload the project or press `Ctrl+Shift+O`.

![The resync popup and the Bazel tool window](https://resources.jetbrains.com/help/img/idea/2025.3/bazel-sync-popup-and-window.png)

You can also reload the project using the Bazel tool window.

  1. In the main menu, go to View | Tool Windows | Bazel.

  2. In the Bazel tool window, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindows.settingSync.svg) Build and Resync Project button.




The Build and Resync Project option also runs a full build as part of the syncing process. This ensures that all generated source dependencies are available.
