[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-tests-in-gradle.html)
[//]: # (Downloaded: 2025-12-17 20:07:15)

# Testing in Gradle

In the Gradle project, you can [create](create-tests.html) and [run](performing-tests.html) tests the same way you do in any other project.

IntelliJ IDEA also lets you [change the default test runner](gradle-settings.html#gradle_tests) for your testing process and even configure a test runner for each test.

### Configure a test runner

  1. In the Gradle tool window, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) to open the [Gradle settings](gradle-settings.html#gradle_tests) page.

  2. In the Run test using list, select one of the following test runner options for the selected Gradle project: 

     * Gradle: IntelliJ IDEA uses Gradle as a default test runner. As an outcome, you get the same test results on the continuous integration (CI) server. Also, tests that are run in the command line will always work in the IDE.

     * IntelliJ IDEA: select this option to delegate the testing process to IntelliJ IDEA. In this case, IntelliJ IDEA uses the [JUnit](https://junit.org/junit5/docs/current/user-guide/#overview-what-is-junit-5) test runner and tests are run much faster due to the incremental compilation.

     * Choose per test: select this option to configure which test runner (Gradle or IntelliJ IDEA) to use specifically per each test.

![Gradle settings: the Run test using list](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_test_runner.png)
  3. Click OK.




### Run Gradle tests

  1. In your Gradle project, in the editor, [create](create-tests.html) or select a test to run.

  2. From the context menu, select Run <test name>. 

Alternatively, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolwindows.toolWindowRun.svg) icon in the left gutter.

![Run Test](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_run_test_gutter.png)

If you selected the [Choose per test](#choose_per_test) option, IntelliJ IDEA displays both Gradle and JUnit test runners for each test in the editor.

![Choose per test](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_choose_per_test.png)

Once you have selected the test runner, IntelliJ IDEA remembers your selection and automatically runs your test using the option you've chosen. If you want to make both options available once again, delete the created run configuration for the test.

If you want to see the code coverage when you run a test, select the Run 'name()' with coverage option. It works for both IntelliJ IDEA and the Gradle test runners.

![The test coverage report](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_test_coverage.png)
  3. IntelliJ IDEA runs the tests with the configured [test runner](#test_runner) and displays the output in the [test tab](viewing-and-exploring-test-results.html) of the Run tool window. 

![Run tool window / run test with Gradle](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_test_runner_output.png)

If you ran tests with the [Gradle test runner](#gradle_test_runner), various Gradle test options, including parallel test execution, are preserved. For more information, refer to [Gradle documentation](https://docs.gradle.org/current/userguide/performance.html#a_run_tests_in_parallel).

You can also generate the Gradle test report ![Open Gradle test report](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.gradleNavigate.svg) and run [internal Gradle test suites](#internal_gradle_testsuits).




### Debug Gradle tests

  1. In your Gradle project, in the editor, create or select a test that you want to debug.

  2. From the context menu, select Debug <test name>. 

![Debug test](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_debug_test.png)
  3. If the Choose per test option is selected in the [Gradle settings](#configure_gradle_test_runner), IntelliJ IDEA disables the Debug Gradle scripts option located inside the [Run/debug configuration](run-debug-gradle.html) and disables the breakpoints in the Gradle scripts. This is done to speed up your debugging process. You can manually enable or disable breakpoints in the Gradle scripts by adding or removing the Debug Gradle scripts option. 

For more information about debugging, refer to the [Gradle debugging](work-with-gradle-tasks.html#debug_gradle) section.




### Run internal Gradle test suites

Sometimes, in the multi-module projects, you might want to see information about Gradle internal tests suites. For example, when tests are run in parallel, you can make IntelliJ IDEA display information about the testing processes. IntelliJ IDEA also displays how many of those processes are working simultaneously.

  1. In the Run tool window, click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.actions.more.svg), select the Test Runner Settings, and then select Show Internal Gradle Test Suites. 

![Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_internal_testuSuites.png)
  2. Rerun the tests to see the test results that include the Gradle internal ones.




22 August 2025

[Run/Debug Configuration: Gradle](run-debug-gradle.html)[Gradle dependencies](work-with-gradle-dependency-diagram.html)
