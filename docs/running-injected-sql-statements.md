[//]: # (Source: https://www.jetbrains.com/help/idea/running-injected-sql-statements.html)
[//]: # (Downloaded: 2025-12-17 19:59:24)

# Injected SQL statements

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




### Temporarily inject a language

  1. Place the caret inside a string literal, tag, or attribute, in which you want to inject a language and press `Alt+Enter` (or use the intention action icon ![Intention action icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.codeInsight.intentionBulb.png)).

  2. Select Inject language or reference and choose the language you want to inject.


![Temporarily inject a language](https://resources.jetbrains.com/help/img/idea/2025.3/sql_injection_comment_html.png)

### Open a code fragment in the dedicated editor section

  1. Place the caret within the injected code piece and press `Alt+Enter` (or use the intention action icon ![Intention action icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.codeInsight.intentionBulb.png)).

  2. Select Edit <language ID> Fragment.

IntelliJ IDEA will open a dedicated editor section for editing the code with the injected language. This editor provides full coding assistance, including code completion, inspections, intentions and code style actions.

![Open a code fragment in the dedicated editor section](https://resources.jetbrains.com/help/img/idea/2025.3/sql_injected_html_editor.png)



### Cancel injections

  1. Place the caret at the code fragment and press `Alt+Enter` (or use the intention action icon ![the Intention action button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.codeInsight.intentionBulb.png)).

  2. Select Uninject language or reference.




To cancel a language injection, you can also delete the injection comment or annotation.

### Configure injection rules

You can configure language injection rules on the Editor | Language Injections settings page `Ctrl+Alt+S`.

All pre-defined injection rules are configured for the Built-in scope. In other words, they are global (and therefore available in all IntelliJ IDEA projects). Custom rules can be configured for the IDE or for one project only. To change the scope of custom injections, use the Move to Project/IDE Scope icon ![the Move to Project/IDE Scope icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.import.svg).

To configure custom injection rules, click the Add icon ![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add a new rule, or copy a predefined rule and change its settings.

![Language injections settings](https://resources.jetbrains.com/help/img/idea/2025.3/db_injections-settings.png)




28 October 2025

[Configure the SQL code style](configure-the-sql-code-style.html)[Cannot connect to a database](connectivity-problems.html)
