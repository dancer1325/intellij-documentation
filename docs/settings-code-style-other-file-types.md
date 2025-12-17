[//]: # (Source: https://www.jetbrains.com/help/idea/settings-code-style-other-file-types.html)
[//]: # (Downloaded: 2025-12-17 20:00:37)

## Scheme

In this area, choose the [code style scheme](configuring-code-style.html) and change it as required. Code style scheme settings are automatically applied every time IntelliJ IDEA generates, refactors, or reformats your code. 

The IDE comes with two pre-defined schemes: the Project scheme and the Default scheme.

  * In the Project scheme, the settings that you configure apply only to your current project.

These settings are stored in the codeStyles folder under .idea and are shared through VCS together with the project.

The IDE creates the folder after you modify code style settings for your project.

  * In the Default scheme (IDE-level scheme), the settings that you configure apply to all existing projects that have the Default code style scheme selected.

These settings are stored in the codestyles folder under the IntelliJ IDEA [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html) and are not shared through VCS.




If you want to use the project code style scheme as your default scheme, you can copy it to the IDE level. The other way around is also possible: you can overwrite your current project settings with the settings from an IDE-level scheme and share them with other members of your team.

Item| Description  
---|---  
Scheme| From this list, select the scheme to be used. The predefined schemes are shown bold. The custom schemes, ones created as copies of the predefined schemes, are in plain text. The location where the scheme is stored is written next to each scheme, for example, the Default scheme is stored in the IDE, the Project scheme is stored in the project.  
![Show Scheme Actions](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)| Click this button to invoke the list of commands to manage the schemes:

  * Copy to IDE: select this option to copy the scheme settings to IntelliJ IDEA.The option is available only for the Project scheme.
  * Export: select this option to export the selected scheme in the IntelliJ IDEA code style XML, Eclipse XML Profile, or EditorConfig format (if the [EditorConfig](editorconfig.html) plugin is enabled).The option is available for the Project and IDE schemes.
  * Import Scheme: select this option to import the scheme of the selected type from the specified location.The option is available for the Project and IDE schemes.
  * Copy to Project: select this option to overwrite your current project code style settings with the settings from the selected IDE code style scheme.The option is available only for IDE schemes.
  * Duplicate: select this option to create a copy of the selected scheme.The option is available only for IDE schemes.
  * Reset: select this option to reset the default or bundled color scheme to the initial defaults shipped with IntelliJ IDEA. This command becomes available only if some changes have been done.The option is available only for IDE schemes.
  * Rename: select this option to change the name of the selected custom scheme. Press `Enter` to save changes, or `Escape` to cancel.The option is available only for IDE schemes.


