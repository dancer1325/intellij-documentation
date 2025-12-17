[//]: # (Source: https://www.jetbrains.com/help/idea/editorconfig.html)
[//]: # (Downloaded: 2025-12-17 19:25:40)

# EditorConfig

To use EditorConfig, make sure the EditorConfig plugin is enabled in the settings. Press `Ctrl+Alt+S` to open settings and then select Plugins. Click the Installed tab. In the search field, type EditorConfig. For more information about plugins, refer to [Managing plugins](managing-plugins.html). 

IntelliJ IDEA allows you to manage all code style settings for each individual set of files with [EditorConfig](https://editorconfig.org/) support.

All you need to do is place an .editorconfig file in the root directory containing the files whose code style you want to define. If you have several code styles in your project (for example, for tests and for production code), you can have several .editorconfig files in corresponding folders in your project. This allows you to follow multiple code style standards at the same time.

All options from the .editorconfig file are applied to the directory where it resides as well as all of its sub-directories on top of the current project code style. If anything is not defined in `.editorconfig` or other `.editorconfig` files located in parent directories, it's taken from the current [code style scheme](configuring-code-style.html). You can find more information about undefined (`unset`) properties in the [EditorConfig](https://editorconfig.org/) documentation.

All options in the .editorconfig file are divided into the following categories:

  * [Standard options](https://github.com/editorconfig/editorconfig/wiki/EditorConfig-Properties) such as `indent_size`, `indent_style`, and so on. These options do not have any domain-specific prefixes.

  * Generic IntelliJ options that have the `ij_` prefix and are applicable to all languages:

    * `ij_visual_guides`

    * `ij_formatter_off_tag`

    * `ij_formatter_on_tag`

    * `ij_formatter_tags_enabled`

    * `ij_wrap_on_typing`

    * `ij_continuation_indent_size`

    * `ij_smart_tabs`

  * Common IntelliJ options are supported by many (but not all) languages. They start with the `ij_any` prefix, for example, `ij_any_brace_style`.

  * IntelliJ language-specific options starting with the `ij_<lang>_` prefix where `<lang>` is the language domain ID (normally a low-case language name), for example, `ij_java_blank_lines_after_imports`.




All IntelliJ .editorconfig properties have corresponding options in the [code style scheme](configuring-code-style.html) and have similar names.

The same options can be defined as a common option and a language-specific option, for example, `ij_<...>_brace_style`. Language-specific options have higher priority over common or generic options.

### Add an .editorconfig file

  1. In the Project tool window `Alt+1`, right-click a sourcethe directory containing the files whose code style you want to define and select New | EditorConfig from the context menu.

  2. Select the properties that you want to define so that IntelliJ IDEA creates stubs for them, or leave all checkboxes empty to add the required properties manually.

Use code completion while filling .editorconfig files.

  3. To preview how changes to your code style settings will impact the actual source files, click ![the eye icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) in the gutter of the .editorconfig file and select a source file on which you want to preview changes. The preview will open on the right.

Make sure that the file you're selecting corresponds to the mask next to which you clicked ![the eye icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg). For example, to preview `[*.java]` files, the preview file should have the .java extension. 

You can make changes in the preview pane to try and test how your configuration changes are reflected without worrying about making unwanted changes to the source code: all these changes are discarded when you close the .editorconfig file.

  4. Reformat your code. You can reformat a [code fragment](reformat-and-rearrange-code.html#reformat_code), a [file](reformat-and-rearrange-code.html#reformat_file), or [all files in a directory](reformat-and-rearrange-code.html#reformat_module_directory).

Alternatively, you can configure the IDE to [reformat your code on save](reformat-and-rearrange-code.html#reformat-on-save).




To quickly learn whether the file currently opened in the editor has any code style options that are overridden by properties in an .editorconfig file, use the Indentation widget in the status bar.

The ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.ide.configFile.svg) icon in the widget indicates that there's an .editorconfig file that overrides some settings from your current code style scheme.

![Indentation widget with EditorConfig icon](https://resources.jetbrains.com/help/img/idea/2025.3/editorconfig-widget.png)

Click the widget:

  * Click Open .editorconfig to open the nearest .editorconfig file which affects the file that you're currently working with.

  * Select Show Files Related to Project to open a list of all .editorconfig files in the project.

  * Click Disable for Project to disable EditorConfig support in your project and use settings from your current code style scheme. You can also [disable EditorConfig support in settings](#disable-editorconfig).


![EditorConfig menu opened from the Indentation widget](https://resources.jetbrains.com/help/img/idea/2025.3/editorconfig-widget-menu.png)

### Export code style to an .editorconfig file

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style.

  2. Select the code style Scheme that you want to export: the [Project](configuring-code-style.html#project-scheme) scheme or one of the [IDE-level schemes](configuring-code-style.html#default-scheme).

  3. Click ![the Show Scheme Actions button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg), select Export and then EditorConfig File. 

![Exporting code style settings as .editorconfig file](https://resources.jetbrains.com/help/img/idea/2025.3/ij_export_editorconfig.png)
  4. Specify the folder to which you want to save the file.




To import code style settings in an .editorconfig file, drag the file to the necessary folder in the Project tool window `Alt+1` or View | Tool Windows | Project).

### Disable EditorConfig support

If you decide to use IDE settings after creating .editorconfig settings files, you can disable EditorConfig support without removing the created .editorconfig files from your project.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style.

  2. Clear the Enable EditorConfig support checkbox.

  3. Apply the changes and close the dialog.




01 December 2025

[Code style schemes](configuring-code-style.html)[Reformat code](reformat-and-rearrange-code.html)
