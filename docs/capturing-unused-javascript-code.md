[//]: # (Source: https://www.jetbrains.com/help/idea/capturing-unused-javascript-code.html)
[//]: # (Downloaded: 2025-12-17 19:19:41)

# Find unused code with coverage

IntelliJ IDEA lets you find unused JavaScript, TypeScript, and CSS code in your client-side applications. When you run an application in the special Code Coverage mode, IntelliJ IDEA creates a report showing how much code in every file and folder was used. Thanks to [source maps](https://code.tutsplus.com/tutorials/source-maps-101--net-29173), this report shows coverage for your source files but not for the compiled code that was actually run in the browser. 

### Run an application in the Code Coverage mode

  1. Create a run/debug configuration of the type JavaScript Debug:

Go to Run | Edit Configurations in the main menu. In the Edit Configurations dialog that opens, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) on the toolbar and select JavaScript Debug from the list. In the [Run/Debug Configuration: JavaScript Debug](run-debug-configuration-javascript-debug.html) dialog that opens, specify the URL address at which the application is running. This URL can be copied from the address bar of your browser. 

Because the JavaScript Debug configuration works only with Chrome, the Code Coverage mode is also available only in this browser.

  2. Choose the newly created configuration in the Select run/debug configuration list on the toolbar and click the Run with Coverage button (![the Run with Coverage button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.runWithCoverage.svg)) next to the list.

![Start app with coverage](https://resources.jetbrains.com/help/img/idea/2025.3/ws_javascript_coverage_run_with_coverage.png)

The URL address specified in the run configuration opens in the browser.

  3. To learn what code was executed during the page load, just load the application and then stop it by clicking the Stop button (![the Stop button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.suspend.svg)) on the toolbar, next to the Run '' with Coverage button (![the Run with Coverage button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.runWithCoverage.svg)), or in the Run tool window. If you need a coverage report for some specific features of your application, trigger these features in the browser and only then click the Stop button (![the Stop button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.suspend.svg)) to stop the application.

  4. View the report in the Coverage tool window. The Project tool window `Alt+1` shows information about the coverage of files and folders. In the editor, the gutter shows green markers next to the lines that were executed and red markers next to those that were not. You can also hover over the line markers and see how many times each line of code was hit.

![Coverage report](https://resources.jetbrains.com/help/img/idea/2025.3/ws_javascript_coverage_report_with_editor.png)



08 September 2025

[View actual HTML DOM](viewing-actual-html-dom.html)[Flow](using-the-flow-type-checker.html)
