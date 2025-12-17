[//]: # (Source: https://www.jetbrains.com/help/idea/using-zen-coding-support.html)
[//]: # (Downloaded: 2025-12-17 20:05:54)

## Enable and configure Emmet

With IntelliJ IDEA, you can use native Emmet templates plus more than 200 additional HTML, CSS, and XSL live templates that are listed under the Zen CSS, Zen HTML, and Zen XSL nodes on the Editor | Live Templates settings page `Ctrl+Alt+S`.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Emmet.

  2. On the [Emmet page](settings-emmet.html) that opens, choose the key to expand Emmet abbreviations with, by default `Tab` is selected.

  3. To enable or disable Emmet in a specific language (HTML, CSS, or JSX), go to Editor | Emmet | <Language> and toggle the Enable <Language> Emmet checkbox. Use the controls on the [Emmet](settings-emmet.html) page to configure Emmet in various language contexts.




IntelliJ IDEA lets you use and customize Emmet live templates, or you can add your custom templates. Suppose you have a template entry with the following template text:

<entry type="$TYPES$">$END$ <entry>

To generate a list of entries, you just need to type `“entry-list<entry[number=$]*5″` and press `Tab`. By default, the `number` attribute will be generated before `type`. To customize the position where it is generated, you need to add the `ATTRS` variable to your template, for example:

<entry type="$TYPES$" $ATTRS$>$END$ <entry>

The `ATTRS` variable must have an empty string as the default value and should be skipped.

### Use live templates with Emmet

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Live Templates.

  2. On the [Live Templates](settings-live-templates.html) page that opens, expand the Zen HTML, Zen CSS, or Zen XSL template group and select the checkboxes next to the templates you want to use.

  3. When you select a template in the list, the focus moves to the [Template Text](settings-live-templates.html#templateTextArea) area where the fields show the settings of the selected template.

  4. In the Template Text field, add the required text and variables to the template body.

  5. Click the Edit Variables button. In the [Edit Template Variables](edit-template-variables-dialog.html) dialog that opens, specify the default variable values in the Default value field and select the Skip if defined checkbox where necessary.



