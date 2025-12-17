[//]: # (Source: https://www.jetbrains.com/help/idea/sharing-live-templates.html)
[//]: # (Downloaded: 2025-12-17 20:02:38)

## Export and import live templates manually

IntelliJ IDEA also lets you export and import all live templates, which may be more convenient than copying individual templates manually.

### Export live templates manually

  1. Choose File | Manage IDE Settings | Export Settings from the menu.

  2. In the Export Settings dialog, make sure that the Live templates (schemes) checkbox is selected and specify the path and name of the archive, where the exported settings will be saved.

Note that the Live templates checkbox appears in the Export Settings dialog if you have at least one custom live template in your project.

  3. Click OK to generate the file based on the exported settings. You can share this file with your team members, or import it on another IntelliJ IDEA installation.




### Import live templates

  1. Select File | Manage IDE Settings | Import Settings from the menu.

  2. Specify the path to the archive with the exported live templates.

  3. In the Select Components to Import dialog, select the Live templates checkbox and click OK. 




After restarting IntelliJ IDEA, you will see the imported live templates on the Editor | Live templates settings page `Ctrl+Alt+S`.
