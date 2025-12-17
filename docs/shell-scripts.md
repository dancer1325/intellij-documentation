[//]: # (Source: https://www.jetbrains.com/help/idea/shell-scripts.html)
[//]: # (Downloaded: 2025-12-17 20:02:41)

# Shell scripts

### Enable the Shell script plugin

This functionality relies on the [Shell script](https://plugins.jetbrains.com/plugin/13122-shell-script) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Shell script plugin, and select the checkbox next to the plugin name.




IntelliJ IDEA provides coding assistance for shell script files: [completion](auto-completing-code.html) (including local paths), highlighting, [quick documentation](viewing-reference-information.html#inline-quick-documentation) textual rename refactoring, and more.

![Coding assistance for shell scripts](https://resources.jetbrains.com/help/img/idea/2025.3/cl_shellscript_assistance.png)

It also includes a special type of [run/debug configurations](run-debug-configuration-shell-script.html) for shell scripts. 

IntelliJ IDEA integrates with several external tools to enhance shell script support:

  * [ShellCheck](https://github.com/koalaman/shellcheck) is a shell script static analysis tool that can detect syntax errors, semantic problems, corner cases, and typical pitfalls. IntelliJ IDEA will prompt you to install it if it is not available.

  * [Shfmt](https://github.com/mvdan/sh) is an external formatter engine for shell scripts. IntelliJ IDEA will suggest installing it when you [reformat code](reformat-and-rearrange-code.html) `Ctrl+Alt+L` of the shell script for the first time.

  * [Explainshell](https://explainshell.com/) is a website that can parse any shell command and provide help text for each argument. Access to it is available via an [intention action](intention-actions.html): press `Alt+Enter` and select Explain shell.




### Configure file types to be recognized as shell scripts

By default, IntelliJ IDEA recognizes files with the following extensions as shell scripts: .sh, .bash, .zsh. However, you can configure IntelliJ IDEA to recognize any file types as shell script files (for example, if you want to edit .csh files).

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Editor | File Types.

  2. In the Recognized File Types list, select Shell Script and add the necessary patterns in the File Name Patterns list below.

  3. Click OK to apply changes.




### Run shell script files

  * When working on a shell script file, click ![The Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) in the gutter. This will run your script in the built-in [Terminal](terminal-emulator.html).




If you want to customize the startup of your script (for example, specify the script and interpreter options), you can also create a Shell Script [run/debug configuration](#shell-scripts-configurations).

If you run a script from the gutter icon and do not specify the shebang in your script, IntelliJ IDEA will use your default system interpreter defined by the `SHELL` environment variable. If you create a Shell Script run/debug configuration for a script file, IntelliJ IDEA will use the interpreter specified in the Interpreter path field of that configuration.

### Create configurations for script files

  1. In the main menu, go to Run | Edit Configurations.

  2. Click ![The Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Shell Script.

  3. Under Execute, select the Script file option.

  4. Specify the path to the script file and options that you want to pass to the script when it is launched. You can also change the interpreter for running the script and additional options for the interpreter.

  5. Click OK to save the run/debug configuration.




### Create configurations for Shell commands

You can create a Shell Script run/debug configuration for simple arbitrary commands without creating a script file. This can be useful, for example, if you want to automatically run this command before another configuration is launched and do not want to create a separate file for it.

  1. In the main menu, go to Run | Edit Configurations.

  2. Click ![The Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Shell Script.

  3. Under Execute, select the Script text option.

  4. Enter the command text and, optionally, change the command working directory.

  5. Click OK to save the run/debug configuration.


![Shell Script run/debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/shell_script_configuration_for_command.png)

If you want to run this command before another configuration (for example, another script) is launched, you can select the created configuration in the [Before launch](run-debug-configurations-dialog.html#before-launch-options) area of another configuration.

15 December 2025

[Rust](rust-plugin.html)[Terraform](terraform.html)
