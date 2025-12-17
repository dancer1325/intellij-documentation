[//]: # (Source: https://www.jetbrains.com/help/idea/sbt-support.html)
[//]: # (Downloaded: 2025-12-17 19:59:42)

## Working with sbt

When you've imported or created your sbt project, you can edit its build.sbt file directly in the editor. In build.sbt you can specify compiler options, information about your subprojects, and also define your tasks and settings. Every time you change the build.sbt file, you need to synchronize your changes with the project model in IntelliJ IDEA.

You can configure the Sync project after changes in the build scripts option to synchronize the changes made to  build.sbt  automatically. To access this option, select File | Settings | Build, Execution, Deployment | Build Tools.

For manual synchronization, use the corresponding action on the _sbt projects_ tool window toolbar: ![Refresh](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg).

Note that any sbt task can be attached to be run before a run configuration.

IntelliJ IDEA also lets you use other build tools such as [Gradle](gradle.html) or [Maven](maven-support.html) to build your Scala project.
