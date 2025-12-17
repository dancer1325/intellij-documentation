[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-language-interpreter.html)
[//]: # (Downloaded: 2025-12-17 19:21:55)

## Add a local interpreter

### Add an interpreter

  1. Open the Project Structure dialog `Ctrl+Alt+Shift+S` and select Modules on the left.

  2. On the Ruby Interpreters page, click the ![add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button and select Interpreter:

![New local interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_local_ruby_interpreter.png)
  3. Provide a path to the Ruby executable, for example:

     * /usr/local/bin/ruby for Ruby installed on macOS using Homebrew.

     * /usr/bin/ruby for Ruby installed on Linux using apt.

     * C:\Ruby26-x64\bin\ruby.exe for Ruby installed on Windows using RubyInstaller.

IntelliJ IDEA will display the added interpreter along with automatically detected interpreters.

To remove the interpreter from the list, select it, and click the ![remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) button.




### Add an interpreter with custom environment

IntelliJ IDEA allows you to use your custom environment for running any Ruby command from within IntelliJ IDEA. To do this, you need to provide environment variable values or a path to a configuration script when adding a local interpreter.

  1. Open the Project Structure dialog `Ctrl+Alt+Shift+S` and select Modules on the left.

  2. On the Ruby Interpreters page, click the ![add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button and select Interpreter with Custom Environment:

  3. In the invoked dialog, provide a path to the Ruby executable as described in [Add an interpreter](#add_local). Then, configure the Custom environment in one of the following ways:

     * Specify the environment variable values directly.

Example: `env API_KEY=123`

     * If you use a shell script to load environment variables, you need to provide an absolute path to this script.

Example: `/bin/bash /Users/jetbrains/sample_app/env.sh`

Note that the *.sh file should have `"$@"` at the end to allow IntelliJ IDEA to pass some commands required for adding an interpreter.

     * If you use [direnv](https://github.com/direnv/direnv) to load and unload environment variables, pass a path to the directory with the .envrc file to the `direnv exec` command.

Example: `direnv exec /Users/jetbrains/sample_app`

     * If you use [Shadowenv](https://github.com/Shopify/shadowenv) to customize your project environment, pass a path to the project directory to the `shadow exec` command.

Example: `shadowenv exec --dir /Users/jetbrains/sample_app --`

Click OK to add an interpreter.

  4. Select the added interpreter and click OK in the Settings dialog.



