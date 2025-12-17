[//]: # (Source: https://www.jetbrains.com/help/idea/quarkus.html)
[//]: # (Downloaded: 2025-12-17 19:56:34)

## Qute

[Qute](https://quarkus.io/guides/qute) is a templating engine for Quarkus. IntelliJ IDEA provides support for Qute, such as code completion, syntax highlighting, finding usages, and more.

For files to be recognized as Qute templates, they must have the .html, .txt, .json, or .yaml extension and must be located in the src/main/resources/templates folder. Additionally, *.qute.* can be used before the extenstion, for example hello.qute.html.

Features provided by IntelliJ IDEA include:

  * Coding assistance for the Qute syntax.

![Qute syntax completion](https://resources.jetbrains.com/help/img/idea/2025.3/quarkus_qute_syntax_completion.png)
  * Completion for the names and methods of declared variables (`Ctrl+Space`), and navigation to their declarations (`Ctrl+B`).

![Qute variable completion](https://resources.jetbrains.com/help/img/idea/2025.3/quarkus_qute_variable_completion.png)
  * Live templates: Type `q` and press `Ctrl+Space` to view available Qute live templates.

![Qute live templates](https://resources.jetbrains.com/help/img/idea/2025.3/quarkus_qute_live_templates.png)

To configure Qute [live templates](using-live-templates.html) or create new ones, open the IDE settings (`Ctrl+Alt+S`) and go to Editor | Live Templates | Qute.




### Navigate to Qute templates

IntelliJ IDEA enables quick navigation to Qute templates from locations in your code where they are referenced.

  1. Open the section of code where you have referenced a Qute template.

This can be a class annotated with `@CheckedTemplate`, a record that implements `io.quarkus.qute.TemplateInstance`, or an injected template.

  2. In the gutter, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.fileTypes.anyType.svg) (Navigate to Qute template).

![Navigate to Qute](https://resources.jetbrains.com/help/img/idea/2025.3/quarkus_navigate_to_template.png)



If the relevant Qute template exists, it will be opened in the new editor tab. IntelliJ IDEA takes into account the `@Location` annotation and the `basePath` attribute when determining the template location.
