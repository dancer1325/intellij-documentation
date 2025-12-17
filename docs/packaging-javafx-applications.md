[//]: # (Source: https://www.jetbrains.com/help/idea/packaging-javafx-applications.html)
[//]: # (Downloaded: 2025-12-17 19:33:45)

## Build JavaFX artifacts

### Create a new artifact configuration

IntelliJ IDEA creates the artifact for packaging the application together with the project. However, you can create a new artifact configuration with your custom settings.

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S` and click Artifacts.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), point to JavaFx Application, and select From module '...'.

![Creating a new artifact configuration](https://resources.jetbrains.com/help/img/idea/2025.3/fx-new-artifact.png)

IntelliJ IDEA creates the artifact configuration and shows its settings in the right-hand part of the Project Structure dialog.

  3. Name the new configuration.

  4. Switch to the JavaFX tab and in the Application class field, specify the `main()` method.

  5. Apply the changes and close the dialog.

![Creating a new artifact configuration: specifying the main class](https://resources.jetbrains.com/help/img/idea/2025.3/fx-new-artifact-main.png)



This is a basic configuration that is sufficient to package an application. You can specify additional options on the JavaFX tab. For the detailed description of each option, refer to [Java FX tab](project-structure-artifacts-java-fx-tab.html).

### Build the artifact

  1. In the main menu, go to Build | Build Artifacts.

  2. In the popup that opens, select the necessary artifact and select Build.




By default, the artifact is generated to <project_folder>\out\artifacts\<artifact_name>.

If you want to make sure that your artifact is built correctly, create a new run configuration and run it as described in the section [Run the packaged application](creating-and-running-your-first-java-application.html#run_jar_artifact).
