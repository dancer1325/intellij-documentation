[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-inspection-severities.html)
[//]: # (Downloaded: 2025-12-17 19:21:49)

# Change inspection severity

Inspection severity levels indicate how seriously the detected code problems affect your project. In IntelliJ IDEA, there is a set of predefined severity levels:

![Error icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.status.error.svg) Error
    

Syntax errors

![Warning icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inspectionsWarningIcon.svg) Warning
    

Code fragments that might produce bugs or require enhancement

![Weak Warning icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inspectionsWeakWarningIcon.svg) Weak Warning
    

Code fragments that can be improved or optimized (redundant code, duplicated code fragments, and so on)

![Server Problem icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inspectionsServerProblemIcon.svg) Server Problem
    

Problems that come from an external build server, for example, from TeamCity

![the Typo icon](https://resources.jetbrains.com/help/img/idea/2025.3/grazie.icons.grammarError.svg) Grammar Error
    

Grammar mistakes. This severity comes from the bundled Natual Languages plugin. For more information, refer to [Grammar](grammar.html).

![the Typo icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.inspectionsTypos.svg) Typo
    

Spelling mistakes and typos. For more information, refer to [Spellchecking](spellchecking.html).

Consideration
    

Code fragments that can be improved. This severity level is not marked on the [error stripe](file-and-project-analysis.html#error_stripe) and does not have a default highlighting style, but you can select one from the list of existing styles or configure your own.

No highlighting (fix available)
    

No code highlighting, but you can invoke fixes by pressing `Alt+Enter`.

For every severity, you can configure its own highlighting style in the editor.

Severity levels are designed to indicate problems, they don't have any impact on the code execution: if you change the severity for spelling mistakes from Typo to Error, this won't affect the execution of your application.

### Change inspection severity in all scopes

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections.

  2. Select the profile that you want to modify and then choose an inspection from the list. Make sure that it is enabled.

  3. From the Severity list, select a new severity level. You can also right-click the inspection and select the severity level from the context menu.

If the necessary severity is not on the list, click Edit Severities to [create a new one](#new_severity).

  4. From the Highlighting in editor list, select the style that you want to use to highlight code fragments in the editor.

Select Edit Highlighting to [modify the existing styles](#change_highlighting).

![Selecting severity level for an inspection](https://resources.jetbrains.com/help/img/idea/2025.3/ij_inspection_severity.png)
  5. Apply the changes and close the dialog. 

The modified inspection will now have the new severity level in the selected profile.




### Change inspection severity in specific scopes

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections.

  2. Select the profile that you want to modify and then choose an inspection from the list. Make sure that it is enabled.

  3. From the Scope list, select the scope for which you want to change the severity.

IntelliJ IDEA shows severities for two scopes: the selected one and Everywhere else.

To add one more scope, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg). If you want to create a new scope, select Edit Scopes Order from the list of scopes and click ![the Edit icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg).

  4. Select the necessary severity level from the Severity list.

If the necessary severity is not on the list, click Edit Severities to [create a new one](#new_severity).

![Changing inspection severity by scope](https://resources.jetbrains.com/help/img/idea/2025.3/severity_by_scope.png)
  5. Additionally, from the Highlighting in editor list, select the style that you want to use to highlight code fragments in the editor.

Select Edit Highlighting to [modify the existing styles](#change_highlighting).




If you enable an inspection in multiple scopes, and files in these scopes match, the IDE will process these scopes according to their order in the list. For more information, refer to [Change the order of scopes](running-inspections.html#scopes_order).

You can quickly change an inspection's severity level to No highlighting (fix available) right in the editor. For more information, refer to [Disable highlighting, but keep the fix](disabling-and-enabling-inspections.html#disable_highlighting_keep_fix).

### Configure error highlighting

  1. Press `Ctrl+Alt+S` to open the IDE settings and select Editor | Color Scheme | General.

You can also configure highlighting from inspection settings: go to Editor | Inspections, click any enabled inspection, and from the Highlighting in editor list, select Edit Highlighting.

  2. From the Errors and Warnings list, select the style that you want to modify.

  3. Configure the new highlighting rules using the options on the right. To preview the changes before applying them, use the preview section at the bottom of the dialog.

![Changing error highlighting](https://resources.jetbrains.com/help/img/idea/2025.3/severity_formatting.png)



### Create a new severity level

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections.

  2. Select the profile in which you want to create a new severity level.

  3. Click any inspection and select Edit severities from the list of severity levels.

  4. In the Severities Editor dialog, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and name the new severity level.

  5. Configure the formatting and set a priority using the ![Up](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moveUp.svg) and ![Down](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moveDown.svg) buttons — the higher you put the severity on the list, the higher its priority.

  6. Click OK when finished. 

![Creating a new severity](https://resources.jetbrains.com/help/img/idea/2025.3/severities_editor_ij.png)



08 October 2025

[Inspection profiles](customizing-profiles.html)[Disable and suppress inspections](disabling-and-enabling-inspections.html)
