[//]: # (Source: https://www.jetbrains.com/help/idea/debug-asynchronous-code.html)
[//]: # (Downloaded: 2025-12-17 19:24:14)

## Async stack traces in the console

By default, async stack traces are shown in the console when you debug code or run [JUnit](junit.html)/[TestNG](testng.html) unit tests.

![Async stack trace printed in the console for a failed test](https://resources.jetbrains.com/help/img/idea/2025.3/async-stack-trace-in-console.png)

You can disable async stack traces for tests by clearing the Print async stack trace for exceptions checkbox in the corresponding run configuration.

!['Print async stack trace for exceptions' checkbox in run configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/async-stack-trace-in-console-remove.png)

For turning async stack traces on or off for debug sessions, use the Instrumenting agent option in the Settings | Build, execution, deployment | Debugger | Async stack traces.
