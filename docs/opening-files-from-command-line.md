[//]: # (Source: https://www.jetbrains.com/help/idea/opening-files-from-command-line.html)
[//]: # (Downloaded: 2025-12-17 19:33:31)

# Open files from the command line

Open an arbitrary file or folder in IntelliJ IDEA from the command line, optionally specifying where to place the caret after opening.

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea64.exe [--line <number>] [--column <number>] <path>

Examples
    

Open a project:

idea64.exe C:\MyProject 

Open a specific file on line number 42:

idea64.exe --line 42 C:\MyProject\scripts\numbers.js 

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea [--line <number>] [--column <number>] <path>

Examples
    

Open a project:

idea ~/MyProject 

Open a specific file on line number 42:

idea --line 42 ~/MyProject/scripts/numbers.js 

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea.sh [--line <number>] [--column <number>] <number> <path>

Examples
    

Open a project:

idea.sh ~/MyProject 

Open a specific file on line number 42:

idea.sh --line 42 ~/MyProject/scripts/numbers.js 

When you specify the path to a file, IntelliJ IDEA opens it in the [LightEdit mode](lightedit-mode.html), unless it belongs to a project that is already open or there is special logic to automatically open or create a project (for example, in case of Maven or Gradle files) . If you specify a directory with an existing project, IntelliJ IDEA opens this project. If you open a directory that is not a part of a project, IntelliJ IDEA adds the .idea directory to it, making it a project.

31 October 2025

[Command-line interface](working-with-the-ide-features-from-command-line.html)[Compare files from the command line](command-line-differences-viewer.html)
