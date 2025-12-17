[//]: # (Source: https://www.jetbrains.com/help/idea/command-line-differences-viewer.html)
[//]: # (Downloaded: 2025-12-17 19:21:05)

# Compare files from the command line

Open the [diff viewer](differences-viewer.html) to compare two or three files from the command line. For example, you can compare the current version of a file with its backup, or your local copy of a file with its copy from the remote repository or its copy from another branch.

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea64.exe diff <path1> <path2> [<path3>] 

Examples
    

Compare two files:

idea64.exe diff C:\MyProject\Readme.md C:\MyProject\Readme.md.bak 

Open a blank diff viewer:

idea64.exe diff 

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea diff <path1> <path2> [<path3>] 

Examples
    

Compare two files:

idea diff ~/MyProject/Readme.md ~/MyProject/Readme.md.bak 

Open a blank diff viewer:

idea diff 

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea.sh diff <path1> <path2> [<path3>] 

Examples
    

Compare two files:

idea.sh diff ~/MyProject/Readme.md ~/MyProject/Readme.md.bak 

Open a blank diff viewer:

idea.sh diff 

08 October 2024

[Open files from the command line](opening-files-from-command-line.html)[Merge files from the command line](command-line-merge-tool.html)
