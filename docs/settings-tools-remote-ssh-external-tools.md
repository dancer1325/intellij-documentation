[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-remote-ssh-external-tools.html)
[//]: # (Downloaded: 2025-12-17 20:02:05)

## Tool Settings

Make sure that you specify the absolute paths for the tool's settings, not paths relative to the project.

Program
    

The absolute path to the executable file (script, utility, application, and so on).

Arguments
    

The arguments passed to the executable file, as you would specify them on the command line.

  * Use spaces to separate individual arguments.

  * Use double quotes for arguments and paths that contain spaces.

  * Use a backslash to escape double quotes that are part of the argument or path.




For example:

-Dmy.prop=\"quoted_value\" "second arg" third" "arg

Working directory
    

The absolute path to the working directory from which the tool should be executed.

You can use [built-in IDE macros](built-in-macros.html) to specify the name of the current file, paths relative to the project root, and other contextual information for the tool.
