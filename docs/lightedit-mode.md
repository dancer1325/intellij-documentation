[//]: # (Source: https://www.jetbrains.com/help/idea/lightedit-mode.html)
[//]: # (Downloaded: 2025-12-17 19:31:22)

## Open a file in LightEdit

You can use several ways to open a file in the LightEdit mode.

If you have a Toolbox installation of IntelliJ IDEA, ensure that you have installed IntelliJ IDEA from the Toolbox 1.9 version. If you have a standalone installation of IntelliJ IDEA, create a command-line launcher (Tools | Create Command Line Launcher) first.

### Open a file from the command line

  * Open the file from the command line using the short `-e` or long `--edit` option before the file name:

idea.bat -e README.md 

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

idea -e README.md 

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

idea.sh -e README.md 

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).




You can open files from the command line in full-edit mode. Learn more from [Open files from the command line](opening-files-from-command-line.html).

### Open and edit a file with the wait switch

You can interrupt a process in the command line and put the terminal on hold until you are done editing a file in the LightEdit mode. For example, when working in the command line and running a Git commit process, you can pause the terminal and use the LightEdit mode to write the commit message.

  * Open the file from the command line using the the `-e` (or `--edit`) and `--wait` options before the name of your file.

idea.bat -e --wait README.md 

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

idea -e --wait README.md 

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

idea.sh -e --wait README.md 

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

IntelliJ IDEA opens the file in LightEdit mode and displays a notification indicating that the command line is waiting for the file to be closed.

![the Command line waiting notification](https://resources.jetbrains.com/help/img/idea/2025.3/open_wait_mode.png)



### Open an empty IDE window in LightEdit

You can open an empty IDE window in the LightEdit mode. From there, you can open the files you want to edit using the File | Open option in the main menu.

  * Depending on your OS, start the IDE by using the `-e` (or `--edit`) option.

idea.bat -e 

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

idea -e 

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

idea.sh -e 

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).



