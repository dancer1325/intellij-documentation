[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-maven-goals.html)
[//]: # (Downloaded: 2025-12-17 20:07:10)

## Run Maven goals

You can use several ways to run Maven goals, such as using the Run Anything window, using the context menu in the Maven tool window, or creating a [run configuration](run-debug-configuration.html) for one or several Maven goals.

### Run a Maven goal from the Run Anything window

  1. In the Maven tool window, on the toolbar, click the ![Execute Maven Goal](https://resources.jetbrains.com/help/img/idea/2025.3/maven.images.executeMavenGoal_dark.svg) button. Alternatively, press `Ctrl` twice to open the Run Anything window. 

![Run Anything dialog](https://resources.jetbrains.com/help/img/idea/2025.3/maven_run_anything.png)
  2. In the Run Anything window, start typing a name of the goal you want to execute. The window also displays a list of recent Maven goal entries. 

If you have a multi-module project and need to execute a goal from the specific module then in the Run Anything window, in the top-right corner, from the Project list, select a module or a directory you need and in the search field enter the goal's name.

If you have options such as `offline mode`, [profiles](work-with-maven-profiles.html), or [skip test](work-with-tests-in-maven.html#skip_test) configured for the project, IntelliJ IDEA will automatically include the configuration into the running scope.

  3. IntelliJ IDEA runs the selected goal and displays the result in the Run tool window. 

![Maven Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/mvn_run_tool_window.png)



### Run a Maven goal from the context menu

  1. In the Maven tool window, click Lifecycle to open a list of Maven goals.

  2. Right-click the desired goal and from the context menu select Run 'name of the goal'. IntelliJ IDEA runs the specified goal and adds it to the Run Configurations node.




### Run a Maven goal or a set of goals via Run configuration

IntelliJ IDEA lets you create a run configuration for one specific goal or a set of several goals.

  1. In the Maven tool window, click Lifecycle to open a list of Maven goals.

  2. Right-click a goal for which you want to create a Run configuration. (To select several Maven goals, press `Ctrl` and highlight the desired goals.)

  3. From the list, select Modify Run Configuration.

  4. In the Create Run/Debug Configuration: 'goal name' dialog, specify the goal settings (you can specify any Maven commands and arguments) and click OK. 

![the context menu](https://resources.jetbrains.com/help/img/idea/2025.3/maven_tool_window_context_menu.png)

IntelliJ IDEA displays the goal under the Run Configurations node. 

![the Run Configurations node](https://resources.jetbrains.com/help/img/idea/2025.3/maven_runConfigurations_display.png)
  5. Double-click the goal to run it or right-click the goal and from the context menu select Run.



