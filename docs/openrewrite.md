[//]: # (Source: https://www.jetbrains.com/help/idea/openrewrite.html)
[//]: # (Downloaded: 2025-12-17 19:33:34)

## OpenRewrite run configuration

IntelliJ IDEA comes with a dedicated OpenRewrite run configuration. When you run a recipe using the gutter icon ![The Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.run.svg) for the first time, IntelliJ IDEA creates a temporary run configuration.

If you want to customize how IntelliJ IDEA launches the recipe, you can modify this run configuration or create a new one: go to Run | Edit Configurations or press `Alt+Shift+F10`.

![OpenRewrite run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/openrewrite_run_configuration.png)

### Main parameters

Name
    

Specify a name for the run configuration.

Store as project file
    

Save the run configuration settings to a file that you can share with other team members. The default location is .idea/runConfigurations. However, if you do not want to share the .idea directory, you can save the configuration to any other directory within the project.

Working directory
    

Directory where you want to run the recipes.

Active recipes
    

Recipes to run. Start typing the name to get completion for your local recipe name and names of applicable recipes from the OpenRewrite catalog.

### Logs

Specify which log files generated while running the application should be displayed in the console on the dedicated tabs of the [Run](run-tool-window.html) tool window.

### OpenRewrite modify options

Active styles
    

List of [OpenRewrite styles](https://docs.openrewrite.org/concepts-explanations/styles) to apply. Similarly to recipes, you can enter the name of your local style, or start typing a name to get completion for styles from the OpenRewrite catalog.

Config location
    

Specify a custom location of the OpenRewrite configuration file.

Exclusions
    

Specify files or paths to exclude OpenRewrite operations, for example `**/internal/**`.

Plain text masks
    

Set of file masks to denote which files should be parsed as plain text.

OpenRewrite version
    

Customize the version of the Maven/Gradle OpenRewrite plugin to be used.

Add VM options
    

VM options to be passed to the Java virtual machine when launching the application.

Environment variables
    

Set environment variables for the Maven goal or the Gradle task used for the OpenRewrite recipe execution.

Dry run
    

Run the [dryRun task](https://docs.openrewrite.org/reference/gradle-plugin-configuration#the-dryrun-task) (for Gradle) or the [dryRun goal](https://docs.openrewrite.org/reference/rewrite-maven-plugin#the-dryrun-goal) (for Maven) to preview the changes that would be made by a recipe, without actually altering any files.

You can locate the path to the Dry run report in the Run tool window.

### Before launch

Select tasks to be performed before starting the selected run/debug configuration.
