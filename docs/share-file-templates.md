[//]: # (Source: https://www.jetbrains.com/help/idea/share-file-templates.html)
[//]: # (Downloaded: 2025-12-17 20:02:34)

# Share file templates

When you create or modify a file template, you do it in one of the following scopes (determined by the Scheme parameter under Editor | File and Code Templates):

  * Default: file templates created at the IDE level. These templates are available in all projects that you open with the current IDE instance. Use them as your personal templates that you prefer regardless of the specific project. IntelliJ IDEA stores global templates in the [IDE configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory) under fileTemplates.

  * Project: file templates specific for the current project. These templates are available to everyone who works on this project. IntelliJ IDEA stores them in the project folder under .idea/fileTemplates.




If you have file templates available at the IDE level (Default scheme), you can share them using Backup and Sync or by manually exporting them.

### Share file templates using Backup and Sync

If you want to synchronize file templates across your IDEs (rather than sharing them with your teammates), you can use [Backup and Sync](sharing-your-ide-settings.html#IDE_settings_sync). Backup and Sync uses the JetBrains server to synchronize IDE settings across the IDEs where you sign in using your JetBrains account.

  1. Press `Ctrl+Alt+S` to open Settings, go to Backup and Sync.

  2. If Backup and Sync is not yet enabled, click Enable Backup and Sync.

  3. To share file templates, make sure the Code settings checkbox is selected under Configure what to sync. Select this checkbox on other IDEs where you want your code settings (including live templates) to be shared.




### Export file templates manually

  1. Choose File | Manage IDE Settings | Export Settings from the menu.

  2. In the Export Settings dialog, make sure that the File templates (schemes) checkbox is selected and specify the path and name of the archive, where the exported settings will be saved.

  3. Click OK to generate the file based on the exported settings. You can share this file with your team members, or import it on another IntelliJ IDEA installation.




### Import file templates

  1. Select File | Manage IDE Settings | Import Settings from the menu.

  2. Specify the path to the archive with the exported file templates.

  3. In the Select Components to Import dialog, select the File templates checkbox and click OK. 




After restarting IntelliJ IDEA, you will see the imported file templates on the Editor | File templates settings page `Ctrl+Alt+S`.

04 April 2025

[Templates with multiple files](templates-with-multiple-files.html)[Read-only files](read-only-files.html)
