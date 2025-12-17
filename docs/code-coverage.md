[//]: # (Source: https://www.jetbrains.com/help/idea/code-coverage.html)
[//]: # (Downloaded: 2025-12-17 19:20:12)

## Run with coverage

The entry points for running coverage analysis are the same as you would normally use to [run an application](running-applications.html):

  * For main method definitions, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) Run in the editor gutter, then select Run with Coverage

![A popup appears on clicking the gutter Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/run-coverage-from-gutter-ij.png)
  * For [run configurations](run-debug-configuration.html), click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg) More Actions in the [Run widget](new-ui.html#window_header), then select Run with Coverage

![A menu appears on clicking More Actions in the Run widget](https://resources.jetbrains.com/help/img/idea/2025.3/run-coverage-from-run-widget-ij.png)
  * For Gradle tasks, go to Gradle tool window, right-click the task, and select Run with Coverage

![A menu appears on clicking a task in Gradle tool window](https://resources.jetbrains.com/help/img/idea/2025.3/run-coverage-for-tasks-ij.png)



Coverage analysis executes the corresponding run configuration with the coverage agent attached. This agent instruments the bytecode to keep track of the execution line-by-line. After the execution completes, the results of the analysis appear in the IDE.
