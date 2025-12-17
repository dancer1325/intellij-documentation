[//]: # (Source: https://www.jetbrains.com/help/idea/maven-ignored-files.html)
[//]: # (Downloaded: 2025-12-17 19:32:06)

# Maven. Ignored Files

Use this page to specify the pom.xml files or their paths of Maven modules, which you want to exclude from the project when you [ignore](delegate-build-and-run-actions-to-maven.html#ignore_maven_project) a Maven subproject.

Item| Description  
---|---  
Path patterns| Enter the comma-separated list of paths to be ignored during the build. Wildcards are honored. For example, entering `*` will ignore all the files in the project. You can use [Maven](maven-projects-tool-window.html#edit_ignored) tool window to edit the specified patterns.  
Ignored files| Check the individual files to be ignored during the build. If you have a multi-module project, IntelliJ IDEA lists all POM files of your project. Selecting the checkbox against a POM file will equal ignoring the project or module in the Maven structure. You can also use the [Maven](maven-projects-tool-window.html#ignore_unignore) tool window to ignore or unignore projects from the importing. To reverse the Ignored files action, clear the checkboxes against the files you don't want to ignore.  
  
23 October 2024

[Maven. Importing](maven-importing.html)[Maven. Runner](maven-runner.html)
