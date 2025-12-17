[//]: # (Source: https://www.jetbrains.com/help/idea/gradle-settings.html)
[//]: # (Downloaded: 2025-12-17 19:28:20)

# Gradle settings

Settings | Build, Execution, Deployment | Gradle

Use this page to configure settings for Gradle projects that were [created](gradle.html#project_create_gradle), [opened](gradle.html#gradle_import_project_start), or [linked](gradle.html#link_gradle_project).

To configure the offline mode, refer to the [Gradle tool window](jetgradle-tool-window.html#offline). If you need to add VM options, refer to the [Gradle VM options](gradle.html#gradle_vm_options).

Item| Description  
---|---  
Gradle user home| Use this field to specify the location for Gradle to store its global configuration properties, initialization scripts, caches, log files, and so on. For more information, refer to [Gradle documentation](https://docs.gradle.org/current/userguide/directory_layout.html#dir:gradle_user_home).The default is set to $USER_HOME/.gradle. It can be overridden in one of the following ways:

  * You can set the `GRADLE_USER_HOME` environment variable (for example, `%APPDATA%\.gradle`). For more information, refer to [Gradle documentation](https://docs.gradle.org/current/userguide/build_environment.html#sec:gradle_environment_variables). The variable's value is picked up automatically. The new path is reflected in the field. You might need to restart your IDE in order for this change to take effect.
  * You can specify the location manually: type the location in the path or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and in the dialog that opens, select the needed directory. Manually entered values take precedence over the environment variables.

If the Gradle location is set in Use Gradle from with the Specified location option and its path is defined in the environment variable `GRADLE_HOME` or `PATH`, IntelliJ IDEA deduces this location and suggests its path as the default value.IntelliJ IDEA also supports the custom Gradle location installed from the [Homebrew](https://docs.gradle.org/current/userguide/installation.html#installing_with_a_package_manager) package manager.  
Generate *.iml files for modules imported from Gradle| Select this option to store the generated .iml and library files in the .idea directory instead of idea.system.path. It might be helpful in the following cases:

  * sharing the IDE-specific module settings via VCS since the .idea directory stores [project-level settings](configure-project-settings.html). You can also opt for the [gradle-idea-ext](https://github.com/JetBrains/gradle-idea-ext-plugin) plugin that helps you describe the [project settings](work-with-gradle-projects.html#project_encodings) in the build.gradle file.
  * correctly opening a project that contains both regular IntelliJ IDEA modules and Gradle modules.
  * accessing a project faster when you open it since IntelliJ IDEA reads the .iml files first and then starts the importing process.

When you make changes in your Gradle project, the .iml files get changed as well so don't forget to push them along with the other project's changes under VCS.  
Enable parallel Gradle model fetching for Gradle 7.4+| Select this option to speed up the project's import.This option is automatically disabled for the newly created projects. It is also disabled in File | New Projects Setup | Settings for New Projects.If you check out a project from VCS that contains the `.idea` folder with already disabled parallel import feature, the project will be opened with the Enable parallel Gradle model fetching for Gradle 7.4+ disabled.  
Gradle projects| You can have several [linked Gradle projects](gradle.html#link_gradle_project) when you work in IntelliJ IDEA. You can configure settings for each selected project.  
Download external annotations for dependencies| When this checkbox is selected, IntelliJ IDEA downloads a file with a set of external annotations from the [JetBrains public repository](https://packages.jetbrains.team/maven/p/ij/intellij-redist/org/jetbrains/externalAnnotations/).  
Build and run| Use this section to specify what IntelliJ IDEA should use when you run tests, build, or run tasks in the selected linked project.  
Build and run using| Use this list to select how you want to [build and run your project](work-with-gradle-projects.html#delegate_build_gradle). Use Gradle as a default option or select IntelliJ IDEA. In this case when you select Build | Build Project from the main menu, IntelliJ IDEA goes through source sets in all modules executing the Gradle task `classes`.![Build output](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_build.png)If you have a pure Java or a Kotlin project, it is sometimes better to select IntelliJ IDEA for building a project. IntelliJ IDEA supports the [incremental build](compiling-applications.html#compile_module) which significantly speeds up the building process. Yet, keep in mind that the IntelliJ IDEA compiler does not support some parts of the Gradle project build processing and might cause problems in building your project correctly.  
Run tests using| Use this list to select how you want to [run tests](work-with-tests-in-gradle.html) in your project. Use Gradle as a default option or select IntelliJ IDEA.  
Gradle|   
Distribution| Use this list to configure a Gradle version for your project. You can select one of the following options:

  * 'gradle-wrapper.properties' file: this is a recommended default option that uses [Gradle wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html). In this case you delegate the update of Gradle versions to Gradle and get an automatic Gradle download for the build. This option also lets you build with a precise Gradle version. The Gradle version is saved in the gradle-wrapper.properties file in the gradle directory of your project and helps you eliminate any Gradle version problems.
  * 'wrapper' task in Gradle build script: select this option to configure a Gradle wrapper according to the `wrapper` task configuration. It might be convenient if you prefer to control which Gradle version to use in the project. If you used the default Gradle wrapper option and then switched to the Gradle `wrapper` task configuration, changes you made in the task automatically update during the project import.
  * Specified location: select this option if you don't want to use the Gradle wrapper and prefer to manually download and use a specific Gradle version instead. Specify the location of your Gradle installation.

  
Gradle JVM| Use this field to specify the JVM under which IntelliJ IDEA will run Gradle when you import the specified Gradle project and when you execute its tasks. The default is set to your project JDK.This field overrides any other Gradle JVM selection. You can check a process of how IntelliJ IDEA selects the Gradle JVM version in the [Gradle JVM selection](gradle-jvm-selection.html) section.  
Gradle JVM Criteria| This section becomes available when the [Gradle daemon toolchain support](https://docs.gradle.org/current/userguide/gradle_daemon.html#configuring_the_daemon_jvm) is enabled. For the information on how to enable the support, refer to [Configure Gradle Daemon toolchains](gradle.html#gradle_daemon_toolchain).You can select the JDK version and vendor for your project.  
  
08 May 2025

[Archetype Catalogs](archetype-catalogs.html)[Gant settings](gant-settings.html)
