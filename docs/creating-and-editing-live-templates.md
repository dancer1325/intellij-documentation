[//]: # (Source: https://www.jetbrains.com/help/idea/creating-and-editing-live-templates.html)
[//]: # (Downloaded: 2025-12-17 19:23:17)

# Create live templates

The following example procedure illustrates how to create a template for a `TODO` comment with the current date and user name.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Live Templates.

  2. Select the template group where you want to create a new live template (for example, other).

If you do not select a template group, the live template will be added to the user group.

  3. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Live Template.

  4. Specify the context in which the template will be available. By default, no context is specified and IntelliJ IDEA displays a message at the bottom of the dialog.

Click Define below the message and select the checkboxes next to applicable contexts.

  5. In the Abbreviation field, specify the characters that will be used to expand the template. For example: `todo`. 

  6. (Optional) In the Description field, describe the template for reference in the future.

For example: `Insert TODO comment with the current date and username`

  7. In the Template text field, specify the body of the template with [variables](template-variables.html). For example:

//TODO $DATE$ $USER$: $END$

  8. Click Edit variables to define the variables using [functions](template-variables.html#predefined_functions):

Name| Expression| Default value| Skip if defined  
---|---|---|---  
DATE| date()| None| Yes  
USER| user()| None| Yes  
  
You can set a default value for cases when the expression fails to evaluate, although these particular functions should always return a valid value. You can also disable the Skip if defined option for a variable to highlight the expanded value and let the user modify it if necessary.

  9. Apply all your changes.

  10. In the editor, type `todo` and press `Tab`.

Depending on the current system date and username, the template should expand to something like:

`//TODO 02.07.2019 jsmith:`




### Create a new template from a fragment of code

  1. In the editor, select the text fragment to create a live template from.

  2. Select Code | Save as Live Template... from the main menu. The list of the live templates opens. In this list, the newly created template has been added to the user group.

  3. Specify an abbreviation for the template, an optional description (to identify what the template is for) and modify the template body. If the template has [variables](template-variables.html) defined, click Edit Variables to configure them.

  4. Click OK to apply the changes.




### Copy an existing template

If you want to reuse the same template in multiple groups, or you want to create a new template based on another one, you can duplicate an existing template.

  1. On the Editor | Live Templates page of the Settings dialog (`Ctrl+Alt+S`) , select the template you want to copy.

  2. Click Duplicate ![The Duplicate button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg) on the toolbar. A new template item is added to the same group as the original, and selected.

  3. Specify a new abbreviation for the template, an optional description (to identify what the template is for), and modify the template body if necessary. If the template has [variables](template-variables.html) defined, click Edit Variables to configure them.

  4. Click OK to apply the changes.




08 October 2024

[Live templates](using-live-templates.html)[Live template variables](template-variables.html)
