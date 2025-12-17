[//]: # (Source: https://www.jetbrains.com/help/idea/getting-started-with-groovy.html)
[//]: # (Downloaded: 2025-12-17 19:28:00)

# Run, debug, and test Groovy

You can create, import, test, and run Groovy applications as you would any other projects.

Before you start working with Groovy, make sure the Groovy plugin is [enabled](managing-plugins.html) in IntelliJ IDEA.

### Create a Groovy project

  1. In the [Project Wizard](new-project-wizard.html), select Groovy.

  2. Besides the name of your project and its location, you can select the following options: 

     * Create Git repository: select this option if you want to create a new Git repository for your sources.

     * Build System: select build system you want to use in your project. For small test-like projects select IntelliJ IDEA. If you want to build with one of the build tools, select [Maven](maven-support.html) or [Gradle](gradle.html).

     * JDK: specify your project SDK.

     * Groovy SDK: specify the Groovy SDK. IntelliJ IDEA expects the standard Groovy SDK layout which is provided with the official distributions available at <http://groovy-lang.org/download.html>. Download the SDK, unpack it into any directory and specify this directory as the library home.

     * Add sample code: select this option to create a file with a simple sample code.

     * Advanced Settings: use this part of the wizard to add the name of a module, its content root, and its location.

![Groovy new project](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_new_project.png)
  3. Click Create.




To import a Groovy project, follow the steps from the [Import a project with settings](import-project-or-module-wizard.html#import-project) section.

### Add Groovy support for an existing project

You can add the Groovy framework support for an existing project. However, if you want to add the Groovy support for a [Gradle](gradle.html) or a [Maven](maven-support.html) project, use their build script files (build.gradle or pom.xml). For more information, refer to the [Gradle](https://docs.gradle.org/current/userguide/groovy_plugin.html) or [Maven](https://groovy.github.io/gmaven/groovy-maven-plugin/) documentation.

  1. In the Project tool window `Alt+1`, select the module to which you want to add the Groovy support.

  2. Press `Ctrl+Shift+A` and type `Add Framework Support`.

Once the action is found, click it to open the Add Framework Support dialog.

  3. In the dialog that opens, select Groovy and click OK.

![the Framework Support dialog](https://resources.jetbrains.com/help/img/idea/2025.3/framework_support_dialog.png)

IntelliJ IDEA adds the Groovy SDK to your project, and you can add Groovy classes and Groovy scripts.




### Check the version of Groovy in a project

You can check which version of Groovy SDK IntelliJ IDEA uses in a project.

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S`.

  2. In the Project Structure dialog, under Platform Settings, select Global Libraries. 

![Project Structure dialog / Global Libraries](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_global_library.png)

If you need to check what Groovy SDK version is used in a module, select Modules, the module's name and click the Dependencies tab. 

![Project Structure dialog / Module page](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_sdk_module.png)



### Change the existing Groovy SDK version in a project

  1. In the Project Structure `Ctrl+Alt+Shift+S` dialog, delete `Ctrl+Y` the existing Groovy SDK version from Global Libraries and from module dependencies (the Modules page).

  2. When the Groovy SDK is removed, IntelliJ IDEA displays a popup suggesting to add the Groovy SDK. 

![Configure Groovy SDK popup](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_sdk_configure_popup.png)

Click the link and set up a new SDK.

  3. If IntelliJ IDEA does not display the popup, in the Project tool window, right-click the name of your project and in the context menu, select Add Framework Support.

  4. In the dialog that opens, from the list of technologies, select Groovy and add a new [Groovy library](#groovy_lib). 

![Add Framework Support dialog](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_add_library_dialog.png)

IntelliJ IDEA creates a global-level library.




### Run a Groovy application

After you entered code, you can run it through IntelliJ IDEA or use the [interactive Groovy console](launching-groovy-interaction-console.html) for quick code evaluation.

  1. Open your application in the editor.

  2. Press `Shift+F10` to execute the application. Alternatively, in the left gutter of the editor, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolwindows.toolWindowRun.svg) icon and select Run 'name'. 

![Run an application](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_run_app_editor.png)
  3. View the result in the Run tool window. 

![Run tool window / run Groovy application](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_run_tool_window.png)



To run a Groovy script, from the context menu in the editor, select Run 'name' `Ctrl+Shift+F10`.

You can also click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolwindows.toolWindowRun.svg) icon on the main toolbar to run your application.

### Debug a Groovy application

  1. Open your Groovy application in the editor.

  2. In the left gutter, set your breakpoints for the lines of code you want to debug. The debugger is aware of the Groovy syntax, and you can evaluate an expression on the breakpoint if you need. 

![Evaluate expression](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_evaluate_expression.png)

For more information about breakpoints, refer to the [Breakpoints](using-breakpoints.html) section. 

  3. If you need, you can access the Run/Debug configurations dialog (Run | Edit Configurations) and adjust the settings, but usually the default settings are enough to successfully start and complete your debugging session.

  4. Press `Shift+F9`. Alternatively, on the main toolbar, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.startDebugger.svg) icon to start a debugging process.

  5. Evaluate the results in the Debug tool window.

For more information about using options in the Debug tool window, refer to the [Debug code](debugging-code.html) section.




When in the debug mode, you can [evaluate any expression](examining-suspended-program.html#evaluating-expressions) by using the Evaluate expression tool, which is accessed by pressing `Alt+F8`. This tool provides code completion in the same way as in the editor, so it's easy to enter any expression.

Sometimes, you may want to step into a particular method, but not the first one which will be invoked. In this case, use Smart step into by pressing `Shift+F7` to choose a particular method.

For more information on debugging, refer to the [Debugging](debugging-code.html) section.

### Test a Groovy application

You can test Groovy applications using [JUnit 4](https://junit.org/junit4/) and [JUnit 5](https://junit.org/junit5/) testing frameworks.

  1. Open a class in the editor, for which you want to create a test and place the caret within the line containing the class declaration.

  2. Press `Ctrl+Shift+T` and select Create New Test.

  3. In the dialog that opens, specify your test settings and click OK. 

![Create a Groovy test](https://resources.jetbrains.com/help/img/idea/2025.3/create_groovy_test.png)
  4. Open the test in the editor, add code and press `Ctrl+Shift+F10` or right-click the test class and from the context menu select Run 'test name'.

  5. IntelliJ IDEA creates a run/debug configuration for the test automatically, but if you want to edit settings in your configuration, click Run | Edit Configurations from the main menu.

  6. In the Run/Debug Configurations dialog, on the right side, specify settings for the test suite and click OK. The configuration has standard options, and you can find further details in the [Run tests](performing-tests.html) section. 

  7. On the main toolbar, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolwindows.toolWindowRun.svg) icon to run the test.

  8. Evaluate the results in the Run tool window.




You can navigate between Groovy tests and test subjects (Navigate | Test / Test Subject). If a test class doesn't yet exist, IntelliJ IDEA suggests to create one.

For deploying your Groovy application, refer to [Working with Application Servers](application-servers-support.html).

For building your Groovy projects IntelliJ IDEA lets you use [Gradle](gradle.html), [Maven](maven-support.html), or IntelliJ IDEA own [builder](https://www.jetbrains.com/help/idea/compiler-and-builder.html).

28 June 2024

[Navigation in Groovy](navigation-in-groovy.html)[Run/Debug Configuration: Groovy](run-debug-configuration-groovy.html)
