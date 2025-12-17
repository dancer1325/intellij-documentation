[//]: # (Source: https://www.jetbrains.com/help/idea/absolute-path-variables.html)
[//]: # (Downloaded: 2025-12-17 19:17:37)

# Path variables

Use path variables to define absolute paths to resources that are not part of a specific project. These external resources may be located in different places on the computers of your teammates. This is why user-defined custom path variables are not stored as [project settings](configure-project-settings.html), but as [global IDE settings](configuring-project-and-ide-settings.html). Once configured, such path variables will have the same value for any project that you open with your instance of IntelliJ IDEA.

You can use path variables to specify paths and command-line arguments for [external tools](configuring-third-party-tools.html) and in some [run configurations](run-debug-configuration.html). For more information, refer to [Built-in IDE macros](built-in-macros.html). 

### Create and use a new path variable

For example, you want to add a locally stored JAR file as a module dependency and share this configuration with your teammates through the VCS.

  1. Press `Ctrl+Alt+S` to open settings and then select Appearance & Behavior | Path Variables.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and enter the name of the new variable and its value, which points to the target directory containing the file on your disk.

  3. Add your JAR file as a [module dependency](working-with-module-dependencies.html#add-a-new-dependency).

  4. Check the .iml file. The dependency is added there using a path variable.




After your team members update their projects from VCS, they will change the value of the variable to point to the required JAR file on their computers.

Refer to the variable as `$var_name$` in fields and configuration files that accept path variables.

IntelliJ IDEA also has the following built-in path variables:

$USER_HOME$
    

The current user's home directory.

$PROJECT_DIR$
    

The current project's root directory.

$MODULE_WORKING_DIR$
    

The current [module's root directory](working-with-projects.html).

$MODULE_IML_DIR$
    

The directory with the current module's .iml file.

### Ignore path variables

Whenever you open or update a project, IntelliJ IDEA checks for unresolved path variables. If the IDE detects any, it will ask you to define values for them. If you are not going to use files or directories with the unresolved path variables, you can add them to the list of ignored variables.

You can also use the list of ignored variables when a program argument passed to the run/debug configuration has the same format as a path variable (for example, an environment variable).

  1. Press `Ctrl+Alt+S` to open settings and then select Appearance & Behavior | Path Variables. 

  2. Add the names that IntelliJ IDEA shouldn't consider to be path variables to the Ignored Variables field.

  3. Click OK to apply the changes.




08 October 2024

[Notifications](notifications.html)[IDE settings backup and sync](sharing-your-ide-settings.html)
