[//]: # (Source: https://www.jetbrains.com/help/idea/rearrange-code.html)
[//]: # (Downloaded: 2025-12-17 19:56:51)

## Configure arrangement rules

You can rearrange your code according to the arrangement rules set in the [Code Style](settings-code-style.html) page of the Settings dialog. You can also create groups (aliases) of rules and refer to them when you create a matching rule. 

### Configure grouping rules

Grouping rules let you keep related class methods together.

  1. Press `Ctrl+Alt+S` to open settings and select Editor | Code Style | Java.

  2. On the Arrangement tab, choose the grouping options in the Grouping rules area.

![Grouping rules example](https://resources.jetbrains.com/help/img/idea/2025.3/ij_grouping_rules.png)

For the Keep dependent methods together option, you can select depth-first order or breadth-first order. The former will arrange the methods according to the nesting hierarchy; the latter will group together the sibling methods from the same nesting level. 




### Create matching rules

Matching rules let you define the order of elements as a list of rules, where every rule has a set of matching conditions, such as modifier or type.

  1. Press `Ctrl+Alt+S` to open settings and select Editor | Code Style | Java.

  2. On the Arrangement tab, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and provide the rule parameters in the Matching rules area.

     * Use the Type and Modifier filters to choose the code constructs and their visibility modifiers that should be regulated by the rule. Note that double-clicking a filter negates the condition.

     * Use the Name field to specify entry names the rule should affect.

This filter matches only entry names, such as property names, method names, class names, and so on. The filter supports regular expressions and uses the [standard syntax](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html). The match is performed against the entire name.

     * To sort code entries alphabetically, select the appropriate Matching rules entry and set the Order field to order by name.

![Matching rules example](https://resources.jetbrains.com/help/img/idea/2025.3/matching_rules_example.png)

You can also [create groups (aliases) of rules](#create-rule-aliases) and refer to them when creating a new matching rule.




### Create rule aliases

With aliases, you can group several arrangement rules into a single entity and refer to it when you are adding a new matching rule.

  1. Press `Ctrl+Alt+S` to open settings and select Editor | Code Style | Java.

  2. On the Arrangement tab, click ![Configure matching rules aliases](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg).

  3. In the Rules Alias Definitions dialog that opens, add a group name and its rules.

     * ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg): adds a new alias.

     * ![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg): removes an existing alias from the list.

     * ![the Duplicate button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg): copies a specified rule sequence to the created alias.

  4. In the Rules alias definitions area, define the rule sequence for the created alias. 

![Rules Alias Definitions](https://resources.jetbrains.com/help/img/idea/2025.3/alias_dialog.png)



The created alias can now be referred to when [adding a matching rule](#create-matching-rules).

![Matching Rules alias example](https://resources.jetbrains.com/help/img/idea/2025.3/matching_rules.png)

### Create section rules

Section rules let you move methods or variables into the sections that you have defined.

  1. Press `Ctrl+Alt+S` to open settings and select Editor | Code Style | Java.

  2. On the Arrangement tab, click ![the Add Section Rule button](https://resources.jetbrains.com/help/img/idea/2025.3/app.codeStyle.AddNewSectionRule.svg) and provide the rule parameters in the Matching rules area.

After the arrangement, methods in the class will be rearranged as specified in the created section rule and will be surrounded by comments.




You can exclude specific files and folders from arrangement. For more information, refer to [Exclude files from reformatting](reformat-and-rearrange-code.html#exclude_file_from_reformat).
