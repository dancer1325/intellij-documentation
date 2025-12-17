[//]: # (Source: https://www.jetbrains.com/help/idea/ui-test-automation.html)
[//]: # (Downloaded: 2025-12-17 20:04:56)

## Test automation features

### Tests recognition

When you open your project, IntelliJ IDEA automatically detects tests written in Selenium, Cypress, or Playwright. The recognized tests can be run by clicking the ![The Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) icon in the gutter, and then [analyzed](#review-test-results)/[debugged](#debug-tests) using IDE's tools.

![Viewing tests](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_selenium_run_tests.png)

![Viewing tests](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_cypress_run_tests.png)

![Viewing tests](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_pw_run_tests.png)

### Coding assistance

Provided coding assistance features include intelligent code completion, [navigation](navigating-through-the-source-code.html), [syntax highlighting](configuring-colors-and-fonts.html), support for framework-specific functions and expressions, and more.

For example, you can start typing the locator or its substring in the code editor, and the auto-completion feature will provide you with a list of elements to select from. Additionally, the selected element will be highlighted in Web Inspector, making it easier to choose the correct locator.

### Locators generation and validation

The Web Inspector tool window allows you to view web applications and capture page elements required for automated tests. When you select the required element on the web page, IntelliJ IDEA generates a unique CSS or XPath locator and helps add it to the source code.

Additionally, IntelliJ IDEA can generate [role-based](playwright.html#role_based_locators_support) locators used in Playwright. These locators are designed to reflect the element’s role (for example, a button or a checkbox), making its identification easier.

![Role-based locator](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_playwright_role_based_locators.png)

Moreover, Web Inspector helps you verify that the locators in your code are valid and point to the correct elements on the web page. Clicking the ![](https://resources.jetbrains.com/help/img/idea/2025.3/aqua-plugin.icons.inlayWebInspector.svg) icon next to the locator in the code editor opens the Web Inspector and selects the corresponding element, thus validating the locator.

For more information about Web Inspector, refer to [Aqua documentation](https://www.jetbrains.com/help/aqua/web-inspector-overview.html).

### Manage run/debug configurations for tests

Run/debug configuration is a set of startup properties that define what to execute and what parameters and environment should be used during the execution.

You can create different sets of [configurations](run-debug-configuration.html) for your tests and switch between them instantly, according to your needs.

![Managing test run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_selenium_run_debug_config.png)

![Managing test run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_cypress_run_debug_config.png)

![Managing test run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_pw_run_debug_config.png)

### Test execution details

Once the tests finish running, you are provided with comprehensive results, including logs and console outputs for each test, so you can easily [explore](viewing-and-exploring-test-results.html) them. You can filter the results to quickly navigate through failed or ignored tests and analyze their execution times.

![Viewing test results](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_selenium_failed_tests.png)

![Viewing test results](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_cypress_failed_tests.png)

![Viewing test results](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_pw_failed_tests.png)

### Debugger

A [debugger](debugging-code.html) is a tool used to test and troubleshoot code. It allows you to run the code step by step and provides you with the information on what happens during each step.

A debugger for Selenium and Playwright tests is available out of the box. You can set [breakpoints](using-breakpoints.html) to pause execution and analyze the code.

A classic "in-IDE" debugging approach is not really applicable to Cypress due to the limitations imposed by the specifics of the framework. However, if you have a use case where the classic approach makes sense, feel free to share it with us using [this](https://youtrack.jetbrains.com/newIssue?project=AQUA&summary=%5BIn-IDE+Cypress+Debugging%5D+%3CSpecify+a+title+here%3E&description=**Description%3A**%0A%3CProvide+a+description+of+your+use+case+and+share+your+thoughts+on+why+you+think+a+classic+%22in-IDE%22+debugging+approach+makes+sense+in+your+particular+case.%3E%0A%0A**Additional+information**%0A%3CFeel+free+to+include+any+relevant+details+such+as+the+context%2C+steps+to+reproduce%2C+screenshots%2C+etc.%3E%0A%0A**IDE**%0A%3CWhat+IDE+do+you+use%3F%3E&c=add+Board+Aqua%3A+PM+%26+Strategy&c=add+Board+Aqua%3A+Content+%26+Marketing&c=Type+Usability+Problem&c=Subsystem+Frameworks&c=Framework+Cypress) form.

![Debugger](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_selenium_debugger.png)

![Debugger](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_pw_debugger.png)
