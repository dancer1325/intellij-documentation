[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-database-user-parameters.html)
[//]: # (Downloaded: 2025-12-17 20:01:55)

# User Parameters

For more information about working with user parameters, refer to the [corresponding chapter of Run queries](run-a-query.html#user_parameters) topic.

Item| Description  
---|---  
Enable in query consoles and SQL files| Apply parameter patterns to SQL in SQL files and query files. You can limit the usage scope at the level of [individual patterns](#usage_scope).If this checkbox is cleared, the patterns are not used in SQL files and query files irrespective of the usage scope that is specified for individual patterns.  
Enable in string literals with SQL injection| Apply parameter patterns to string literals [injected](using-language-injections.html) with SQL. If necessary, you can limit the usage scope at the level of [individual patterns](#usage_scope).If this checkbox is cleared, the patterns are not used in string literals irrespective of the usage scope that is specified for individual patterns.  
Substitute inside SQL strings| Apply parameter patterns to string literals in the SQL code.For example, consider the following code.SELECT ${column_name} FROM actor WHERE actor_id='${actor_id}'If the checkbox is cleared, IntelliJ IDEA will find only the `column_name` parameter in it. The `actor_id` parameter is treated as a string.But if you select the Substitute inside SQL strings option, the `actor_id` parameter is treated as a user parameter.![The Substitute inside SQL strings setting disabled](https://resources.jetbrains.com/help/img/idea/2025.3/db_settings_substitute_inside_sql_strings_off.png)![The Substitute inside SQL strings setting enabled](https://resources.jetbrains.com/help/img/idea/2025.3/db_settings_substitute_inside_sql_strings_on.png)  
Parameter patterns| List of parameter patterns and their usage scopes.The patterns are specified using regular expressions. Values that are located in parentheses `()` are treated as parameter names. The patterns available initially have the following meanings:

  * `\?(\d+)` \- a question mark followed by one or more digits, for example, `?69` in which case `69` would be the parameter name.
  * `%\w+` \- `%` followed by one or more word characters, for example, `%xyz`.
  * `\$\{([^$\{\}]*)\}` \- `$`, then `{`, then any character except `$`, `{` or `}` zero or more times, then `}`, for example, `${}`, `${value}`.
  * `\$\(([^\)]+)\)` \- `$`, then `(`, then any character except `)` one or more times, then `)`, for example, $(x).
  * `\$(\w+)\$` \- `$`, then one or more word characters, then `$` again, for example, `$x1$`.
  * `\#(\w+)\#` \- `#`, then one or more word characters, then `#` again, for example, `#field_3#`.

For more information about parameter naming behavior, refer to [Naming behavior](run-a-query.html#naming_behavior).Use ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) `Alt+Insert`, ![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) `Alt+Delete`, ![the Previous Occurrence button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg) `Alt+Up` and ![the Next Occurrence button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg) `Alt+Down` to add, delete and reorder the patterns.To edit a pattern or its usage scope, click the pattern and use the following controls:

  * In scripts: clear this checkbox if the pattern must not be used in SQL files and query files.
  * In literals: clear this checkbox if the pattern must not be used in string literals injected with SQL.
  * All languages: click the link and clear language checkboxes where you do not want to use the pattern.

  
  
02 October 2025

[Output and Results](output-and-results.html)[Data Editor and Viewer](settings-tools-database-data-views.html)
