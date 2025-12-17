[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-projects.html)
[//]: # (Downloaded: 2025-12-17 20:07:27)

## Project, module, and global settings

There are 3 types of settings in IntelliJ IDEA: module, project, and global settings.

![Types of settings](https://resources.jetbrains.com/help/img/idea/2025.3/settings-types.png)

Module settings
    

These settings apply only to one module and are stored in the .iml file. A module can have an SDK and a language level that are different from those configured for a project, and their own libraries. They can also carry a specific technology or a framework.

For more information, refer to [Module structure settings](configure-modules.html).

Project settings
    

These settings apply only to the current project. They are stored together with other project files in the .idea directory in the .xml format. For example, projects keep VCS settings, SDKs, code style and spellchecker settings, compiler output, libraries that are available for all modules within a project.

For more information, refer to [Project settings](configure-project-settings.html) and [Project structure settings](project-settings-and-structure.html).

Global settings
    

Global settings apply to all projects of a specific installation of IntelliJ IDEA. Such settings include IDE appearance (for example, themes and color schemes), the set of installed and enabled plugins, debugger settings, global inspection profiles, and much more.

For more information, refer to [IDE configuration](configuring-project-and-ide-settings.html).
