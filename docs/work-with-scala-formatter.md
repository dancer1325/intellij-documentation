[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-scala-formatter.html)
[//]: # (Downloaded: 2025-12-17 20:07:12)

## Configure Scalafmt

To configure the Scalafmt formatter, in the Settings dialog (`Ctrl+Alt+S`) , go to Editor | Code Style | Scala, and select Scalafmt from the Formatter drop-down list. You will see that the list of tabs under the formatter field has changed.

![Scalafmt settings](https://resources.jetbrains.com/help/img/idea/2025.3/scalafmt_settings.png)

Scalafmt has the following formatting options:

  * Use IntelliJ formatter for code range formatting: this option is selected by default. When you reformat a code selection in the editor, it will be reformatted with the default IntelliJ IDEA formatter. The code selection formatting is also applied to code snippets generated with various actions and [live templates](using-live-templates.html). The Scalafmt formatter can only reformat the entire file.

  * Reformat on file save: if you select this option, IntelliJ IDEA reformats a file when you save it `Ctrl+S`, switch between the active editor and tool windows, or [execute a run/debug configuration](run-debug-and-test-scala.html).

  * Configuration: if IntelliJ IDEA does not find the .scalafmt.conf file with the specified formatter version in your project, it uses the current [default Scalafmt version](https://github.com/scalameta/scalafmt/blob/v1.5.1/scalafmt-core/shared/src/main/scala/org/scalafmt/config/Settings.scala#L19). You can [override the default version](#change_scalafmt).



