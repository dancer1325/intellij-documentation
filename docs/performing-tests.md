[//]: # (Source: https://www.jetbrains.com/help/idea/performing-tests.html)
[//]: # (Downloaded: 2025-12-17 19:33:51)

## Run tests after commit

When you want to check that your changes would not break the code before pushing them, you can do that by running tests as commit checks.

This feature is only available for [Git](using-git-integration.html) and [Mercurial](using-mercurial-integration.html).

### Set up test configuration

  1. Press `Alt+0` to open the Commit tool window and click Show Commit Options ![the Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg).

  2. Under the Advanced Commit Checks menu, next to the Run Tests option, click Choose configuration and select which configuration you want to run. This can be a test configuration provided by your build tool, for example, `gradle test` or a single test class from the project. 

![Pre-commit checks menu](https://resources.jetbrains.com/help/img/idea/2025.3/run-tests-before-commit-0.png)



After you have set up the test configuration, the specified tests will run every time you make a commit.
