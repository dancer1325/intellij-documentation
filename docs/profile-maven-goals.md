[//]: # (Source: https://www.jetbrains.com/help/idea/profile-maven-goals.html)
[//]: # (Downloaded: 2025-12-17 19:56:08)

## Limitations

Currently, there are several limitations for profiling Maven goals:

  * Profiling tools in IntelliJ IDEA do not support Maven profiles, executions, and versions. That is why, some complex configurations might not profile correctly.

  * Profiling of specific versions of the mentioned goals is not supported (for example: `org.codehaus.mojo:exec-maven-plugin:3.0.0:exec`).

  * You cannot profile the goals if they are configured in a way that more than one process is created during their execution.

  * Profiling of the `exec:exec`, `surefire:test`, and `failsafe:integration-test` goals is possible only in projects without modules. You can, however, profile a specific module provided that it has no sub-modules.

  * Profiling is not possible if there are certain arguments in a plugin configuration:

    * `commandlineArgs` in the `exec:exec` plugin configuration

    * `debugForkedProcess` in the `surefire:test` and `failsafe:integration-test` plugin configurations

  * If the Exec Maven Plugin configuration has `<arguments>` in pom.xml, the values in `<arguments>` are skipped during the execution of the `exec:exec` goal.



