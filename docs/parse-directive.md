[//]: # (Source: https://www.jetbrains.com/help/idea/parse-directive.html)
[//]: # (Downloaded: 2025-12-17 19:33:47)

# Reusable content in templates

Include templates are used to define reusable pieces of code (for example, standard headers, copyright statements, and so on) to be inserted in other templates by means of the `#parse` directives. 

The `#parse` directive has the following syntax:

#parse("<include_template_name.extension>")

For example:

#parse("File Header.java")

Templates that can be referenced in this way in other templates are listed on the Includes tab of the Editor | File and Code Templates settings page `Ctrl+Alt+S`.

### Create an include template

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | File and Code Templates.

  2. Open the Includes tab.

  3. Click Create Template ![Create Template](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) on the toolbar and specify the include template name, extension, and body.




### Insert a reusable template into another template

  * Add the `#parse` directive with the name of the include template that you want to insert. For an example, refer to [template syntax](using-file-and-code-templates.html#syntax).




11 October 2024

[File template variables](file-template-variables.html)[Templates with multiple files](templates-with-multiple-files.html)
