[//]: # (Source: https://www.jetbrains.com/help/idea/command-line-formatter.html)
[//]: # (Downloaded: 2025-12-17 19:21:06)

## Options

Option| Description  
---|---  
`-h`| Show the help message and quit.  
`-m|-mask`| Specify a comma-separated list of file masks that define the files to be processed. You can use the `*` (any string) and `?` (any single character) wildcards.  
`-r|-R`| Process specified directories recursively.  
`-s|-settings`| Specify the code style settings file to use for formatting. This can be one of the following:

  * A file with the exported code style settings: open the Editor | Code Style settings page `Ctrl+Alt+S`, click ![The Show Scheme Actions button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg), and select Export.
  * The .idea/codeStyleSettings.xml file stored in your project directory (for IntelliJ IDEA version 2017.2 and earlier).
  * The .idea/codeStyles/Project.xml file stored in your project directory (for IntelliJ IDEA version 2017.3 and later).

The formatter also looks for .editorconfig files in the parent directories and applies them for formatting on top of the IntelliJ IDEA code style settings. In this case, if formatting settings from EditorConfig overlap with the settings from your code style scheme, IntelliJ IDEA will use the settings from EditorConfig. The remaining settings will be taken from your code style scheme. For more information, refer to [EditorConfig](editorconfig.html).If this option is not specified, the file will be skipped. If there is a project in one of the parent folders, its settings will be used implicitly as well as EditorConfig.  
`-allowDefaults`| Use the default code style settings when the code style is not defined for a file or a group of files: when `-s` is not set and the file does not belong to any project. Otherwise, the file or files will be ignored.  
`-charset`| Preserve encoding and enforce the charset for reading and writing source files, for example: `-charset ISO-8859-15`.This option is useful if the command-line formatter cannot correctly process special letters in a source file.  
`-d|-dry`| Run the formatter in the validation mode. The formatter will perform the same formatting operations in memory and will exit with a non-zero status in case any of the formatted files differs from the original one.
