[//]: # (Source: https://www.jetbrains.com/help/idea/maven-importing.html)
[//]: # (Downloaded: 2025-12-17 19:32:07)

# Maven. Importing

Item| Description  
---|---  
Detect compiler automatically| When this option is selected, IntelliJ IDEA uses the compiler that was automatically detected and is specified in the Use compiler list in Settings| Build, Execution, Deployment | Compiler | Java Compiler. Unselect this option if you want to manually specify the compiler.  
Exclude build directory PROJECT_ROOT/target| Select this checkbox to exclude a build directory from the project. This might be useful if you want to speed up the project's importing process. If this checkbox is cleared, IntelliJ IDEA will index files in the build directory every time you import a project, which might take additional time.  
Use Maven output directories| If this checkbox is not selected, the build will be created in the regular IntelliJ IDEA's output directory USER_HOME\IdeaProjects\<project>\classes\Production\. If this checkbox is selected, the build is generated in the Maven's output directory, and the results of IntelliJ IDEA's compilation are reused. However, IntelliJ IDEA itself does not reuse Maven build results, and performs compilation from scratch.  
Generated sources folders| Specify the directory of your source root when you reimport a project.You can select one of the following options:

  * Detect automatically This is a default option. When you select this option, IntelliJ IDEA automatically detects the location of the generated sources. IntelliJ IDEA also detects which directory to mark as a source root. However, IntelliJ IDEA searches for the generated sources only in target/generated-sources and target/generated-sources/* directories.
  * target/generated-sources This option enables you to mark the directory as source root manually.
  * subdirectories of "target/generated-sources" This option enables you to mark a subdirectory as a source root manually.
  * Don't detect This option lets you skip the detection process.

  
Phase to be used for folders update| Select a Maven phase to be used for folder update. This might be useful if you adjust your plugins so that additional sources are loaded at some phase.  
Automatically download| Select the corresponding checkboxes to automatically download sources (Sources) and documentation comments (Documentation) on opening Maven projects.You can select the Annotations option that lets you automatically download custom annotations. IntelliJ IDEA searches for those annotations in the [JetBrains repository](https://packages.jetbrains.team/maven/p/ij/intellij-redist) and downloads them as Maven artifacts during the project's import.  
Dependency types| Use this field to specify dependency types that you want to include when you reimport your project.  
VM options for importer| Use this field to specify VM options. The default option is `-Xmx512m`.When you specify the options, follow the following rules:

  * Use spaces to separate individual options, for example, `-client -ea -Xmx1024m`.
  * If an option includes spaces, enclose the spaces or the argument that contains the spaces in double quotes, for example, `some" "arg` or `"some arg"`.
  * If an option includes double quotes (for example, as part of the argument), escape the double quotes by using the backslashes, for example, `-Dmy.prop=\"quoted_value\"`.

  
JDK for importer| Use this list to specify which JDK to use when the maven project is [imported](maven-support.html#maven_importer).You can choose one of the following options:

  * Internal JRE: this is a default option that uses the installation directory for JRE.
  * JDK versions: this option uses your project's JDK.
  * Use JAVA_HOME: this option uses the value that is specified in the user's environment variable settings.

  
  
25 November 2024

[Maven](maven.html)[Maven. Ignored Files](maven-ignored-files.html)
