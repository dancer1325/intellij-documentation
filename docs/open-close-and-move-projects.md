[//]: # (Source: https://www.jetbrains.com/help/idea/open-close-and-move-projects.html)
[//]: # (Downloaded: 2025-12-17 19:33:26)

## Open and reopen projects

### Open a project

  * Click Open on the Welcome screen.

  * In the main menu, go to File and click Open or Recent Projects if you have worked with the project lately.

Alternatively, you can [open projects from the command line](opening-files-from-command-line.html).




If you are opening a project for the first time, and this project has several configurations (for example Eclipse and Maven), the IDE will ask you which configuration to load. For more information about opening a project correctly, refer to [Open a project (simple import)](import-project-or-module-wizard.html#open-project).

### Open projects in a new or the same window

By default, when you launch the second or any subsequent project, the IDE asks you how you want to open it: in a new window or in the same window. You can configure the default behavior for such cases in the settings:

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Appearance & Behavior | System Settings.

  2. In the Project section, select the necessary Open project in option:

     * New window: open every project in a separate window.

     * Current window: close the current project and open a new one in the same window.

     * Ask: show a dialog with actions to choose from.

![the System Settings page in Settings](https://resources.jetbrains.com/help/img/idea/2025.3/open-reopen-projects.png)
  3. Apply the changes and close the dialog.




### Always reopen projects

If you quit the IDE having multiple opened projects, they all will be reopened the next time you launch IntelliJ IDEA. If you don't want to automatically reopen your projects, you can change this behavior in the settings:

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Appearance & Behavior | System Settings.

  2. In the Project section, clear the Reopen projects on startup checkbox. 

  3. Apply the changes and close the dialog.



