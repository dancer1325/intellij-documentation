[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-line-endings-and-line-separators.html)
[//]: # (Downloaded: 2025-12-17 19:21:57)

# Line separators

With IntelliJ IDEA, you can set up line separators (line endings) for newly created files and change the line separator style for existing files.

### Configure line separators for new files

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style. 

To configure line separators [for new projects](configure-project-settings.html#new-default-settings), go to File | New Projects Setup | Settings for New Projects | Editor | Code Style.

  2. Select the code style Scheme that you want to modify: the [Project](configuring-code-style.html#project-scheme) scheme or one of the [IDE-level schemes](configuring-code-style.html#default-scheme).

  3. From the Line separator list, select the line separator style you want to apply.

     * System-Dependent: select this option to use the separator default for your OS.

     * Unix and macOS ( ): select this option to use the Unix and macOS line separator.

     * Windows ( ): select this option to use the Windows line separator.

     * Classic Mac OS ( ): select this option to use the `\r` line separator, which was used in [Classic Mac OS](https://en.wikipedia.org/wiki/Classic_Mac_OS) (up to Mac OS 9).

  4. Apply the changes and close the dialog. 

![Line Separator for new files](https://resources.jetbrains.com/help/img/idea/2025.3/lineSeparatorForNewFiles.png)



### Change line separators for the current file

The line separator widget appears in the [status bar](guided-tour-around-the-user-interface.html#status-bar) of the IDE window when a file is open in the editor.

  * Click the widget and select another line separator style.

![current line separator](https://resources.jetbrains.com/help/img/idea/2025.3/uiStatusLineEnding.png)
  * Alternatively, select another ending style in File | File Properties | Line Separators.




Changing the line separator style is reflected in the [Local history](local-history.html) of a file.

If you cannot see the line separator widget in the status bar, go to View | Appearance | Status Bar Widgets in the main menu and enable the Line Separators option.

### Change line separators for a file or directory

  1. In the Project tool window (`Alt+1` or View | Tool Windows | Project), select a file or a directory.

If you select a directory, the new line-ending style will be applied to all nested files recursively.

  2. In the main menu, go to File | File Properties | Line Separators, and then select a line-ending style from the list.




Run the Inconsistent line separators inspection to find out which files use line separator that differs from the project's default . Learn more about running inspections from [Run a single inspection](running-inspections.html#run-one-inspection). 

17 November 2025

[Rearrange code](rearrange-code.html)[Indentation](indentation.html)
