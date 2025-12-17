[//]: # (Source: https://www.jetbrains.com/help/idea/disabling-and-enabling-inspections.html)
[//]: # (Downloaded: 2025-12-17 19:25:02)

## Disable inspections

When you disable an inspection, you turn it off. It means that the code analysis engine stops searching project files for the problem that this inspection is designed to detect. Note that when you disable an inspection, you disable it in the current inspection profile; it remains enabled in other profiles.

Most inspections in IntelliJ IDEA can be disabled. However, some inspections will keep highlighting your code regardless of the settings. For example, syntax errors are always highlighted.

### Disable an inspection in settings

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections.

  2. Locate the inspection you want to disable and clear the checkbox next to it. 

  3. Apply the changes and close the dialog. 




You can quickly disable a triggered inspection directly in the editor using a context action.

### Disable an inspection from the editor

  1. Place the caret at the highlighted line and press `Alt+Enter` (or click ![the Show Context Actions icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.codeInsight.intentionBulb.svg)) to invoke a list of available context actions.

  2. Click ![the More Actions button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) next to the inspection you want to disable and select Disable inspection.




### Disable an inspection from the Problems tool window

  1. In the Inspection Results tab of the Problems tool window (appears once you run code analysis), right-click the inspection you want to disable and select Disable inspection.

  2. Click ![the View Options button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) on the toolbar and select Filter resolved items to hide the disabled inspection alerts.




### Re-enable inspections

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections. 

You can also press `Ctrl+Alt+Shift+H` and select Configure Inspections.

  2. Locate the disabled inspection in the list and select the checkbox next to it.

Modified inspections are written in blue. You can also click ![the Filter Inspection button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) and select Show Only Modified Inspections to display only the inspections with changed settings.

  3. Click OK to apply the changes.



