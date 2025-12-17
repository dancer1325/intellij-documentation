[//]: # (Source: https://www.jetbrains.com/help/idea/scheduled-tasks.html)
[//]: # (Downloaded: 2025-12-17 19:59:49)

## Cron expression support

IntelliJ IDEA provides coding assistance and human-readable descriptions for cron expressions in scheduled Spring, Quarkus, and Micronaut services.

### Enable the Cron Expressions plugin

This functionality relies on the [Cron Expressions](https://plugins.jetbrains.com/plugin/24438-cron-expressions) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Cron Expressions plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Cron Expressions plugin, and select the checkbox next to the plugin name.




When you use cron expressions in scheduled tasks, the cron expression language is [injected](using-language-injections.html) providing you with corresponding coding assistance, such as completion and syntax validation. Human-readable explanations appear in inlay hints, making it easier to quickly understand and verify cron expressions.

![Cron expression explanations](https://resources.jetbrains.com/help/img/idea/2025.3/spring_cron_injected.png)

To get a list of cron expression examples, press `Ctrl+Space` after the `cron` keyword.

![Cron expression examples](https://resources.jetbrains.com/help/img/idea/2025.3/spring_cron_examples.png)
