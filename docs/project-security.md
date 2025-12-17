[//]: # (Source: https://www.jetbrains.com/help/idea/project-security.html)
[//]: # (Downloaded: 2025-12-17 19:56:15)

## Open a project from unknown sources

When you open any project, IntelliJ IDEA immediately lets you decide how to handle a project that contains unfamiliar source code.

Every time you open a project for the first time, the IDE shows the Trust Project dialog. This helps to ensure that the project is safe to perform the following actions:

![Untrusted Project](https://resources.jetbrains.com/help/img/idea/2025.3/untrusted_project_first_open.png)

You can select one of the following actions:

  * Preview in Safe Mode: in this case, IntelliJ IDEA opens the project in Safe Mode, meaning you can browse the project's sources, but there are restrictions in executing code, performing build-related activities, and running scripts. 

For more information about Safe Mode preview limitations, refer to [Safe mode preview limitations](#safe_mode_limitations).

IntelliJ IDEA notifies you about Safe Mode on top of the editor area.

![the Trust project notification](https://resources.jetbrains.com/help/img/idea/2025.3/editor_notification.png)

If at this point you want to trust a project, click the Trust project link and load your project.

Alternatively, in the main menu, go to Navigate | Search Everywhere or press `Shift` twice to open the search window and type Trust project.

  * Trust Project: in this case, IntelliJ IDEA opens and initializes the project, resolves project plugins, adds dependencies, and enables all IntelliJ IDEA features.

  * Don't Open: in this case, IntelliJ IDEA cancels the action.




Select the Trust all projects in '<path>' folder checkbox to trust the directory from which you are trying to open the project. The next time you open a project from that directory, it will be opened and loaded automatically.

For Windows, the Add IDE 'project...' folders to Microsoft Defender exclusion list option is available. You can use it to exclude certain project directories from scanning, which may improve the IDE performance.
