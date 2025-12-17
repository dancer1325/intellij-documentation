[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-the-ide-features-from-command-line.html)
[//]: # (Downloaded: 2025-12-17 20:07:34)

## Launcher for a standalone instance

The installation directory contains batch scripts and executables for launching IntelliJ IDEA, formatting the source code, and running inspections. To use them from the Command Prompt cmd.exe, add the location of the IntelliJ IDEA bin folder to the `PATH` environment variable. For example, if you installed IntelliJ IDEA to C:\Program Files\JetBrains\IntelliJ IDEA, you can use the following command:

set PATH=%PATH%;C:\Program Files\JetBrains\IntelliJ IDEA\bin 

This command changes the `PATH` environment variable for the current shell only (the current instance of cmd.exe). If you want to update it permanently for the current user, run `setx`:

setx PATH "%PATH%;C:\Program Files\JetBrains\IntelliJ IDEA\bin" 

To update it system-wide for all users, run `setx /M` instead of `setx`.

The installer can do this for you if you select Add launchers dir to the PATH on the Installation Options step of the setup wizard.

After you configure the `PATH` variable, you can run the executable from any working directory in the Command Prompt:

idea64.exe 

Alternatively, you can use the batch script:

idea.bat 

To run IntelliJ IDEA from the shell, use the `open` command with the following options:

`-a`
    

Specify the application.

`-n`
    

Open a new instance of the application even if one is already running.

`--args`
    

Specify additional arguments to pass to the application.

For example, you can run IntelliJ IDEA.app with the following command:

open -na "IntelliJ IDEA.app" 

If IntelliJ IDEA is not in the default /Applications directory, specify the full path to it.

You can create a shell script with this command in a directory from your `PATH` environment variable. For example, create the file /usr/local/bin/idea with the following contents:

#!/bin/sh open -na "IntelliJ IDEA.app" --args "$@" 

Make sure you have permissions to execute the script and since /usr/local/bin should be in the `PATH` environment variable by default, you should be able to run `idea` from anywhere in the shell.

If you do not have permissions to execute the script, run the following:

chmod +x /usr/local/bin/idea 

On Linux, the installation directory contains the launcher shell script idea.sh under bin. For example, if you installed IntelliJ IDEA to /opt/idea, you can run the script using the following command:

/opt/idea/bin/idea.sh 

You can create a symbolic link to the launcher script in a directory from the `PATH` environment variable. For example, if you want to create a link named idea in /usr/local/bin, run the following command:

ln -s /opt/idea/bin/idea.sh /usr/local/bin/idea 

Since /usr/local/bin should be in the `PATH` environment variable by default, you should be able to run the `idea` command from anywhere in the shell.

If you [installed IntelliJ IDEA as a snap package](installation-guide.html#snap), you can use the corresponding launcher: `intellij-idea`. 
