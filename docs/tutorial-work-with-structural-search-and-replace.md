[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-work-with-structural-search-and-replace.html)
[//]: # (Downloaded: 2025-12-17 20:04:51)

# Work with structural search and replace

The structural search and replace is a powerful tool that can search for a specific pattern of code and add modifiers that can narrow your search.

In this tutorial we will search for field declarations, add modifiers, and create a code inspection based on the modified template. If you want, you can watch the related video before we dive in. The video might slightly differ since it was done for the earlier version of IntelliJ IDEA.

Let's open the Search Structurally dialog and use one of the existing templates for our search.

### Use an existing template (field declaration)

  1. In the main menu, go to Edit | Find | Search Structurally.

  2. In the Structural Search dialog, under the Java | Class-based node, select All Fields of a Class which will look for all field declarations and click Find. 

![the Existing Templates dialog](https://resources.jetbrains.com/help/img/idea/2025.3/all_fields_of_a_class.png)

As a result, in the Find tool window, IntelliJ IDEA shows all the fields declared in our Java code.

![Find tool window: search results](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_result_find.png)



Now, let's return to our structural search dialog to alter the predefined template a bit. By the way, we can use the Search Everywhere window to access the search dialog.

### Alter the predefined template

  1. Press `Shift` twice to open the Search Everywhere window.

  2. Start typing the search query, click Search Structurally in the list of the search results to open our structural search dialog. 

![Search Everywhere window](https://resources.jetbrains.com/help/img/idea/2025.3/search_everywhere_ssr.png)
  3. In the Structural Search dialog, let's update our template to search only for the final fields, by adding `final` before the `$Field$` variable. Notice that the code completion is supported in the dialog. 

![Code completion in the Structural Search dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_code_completion.png)
  4. We'll search for our code recursively, match the case, and search only in Java type files. 

![Structural Search dialog: narrow search](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_search_checkboxes.png)
  5. When we change the scope, IntelliJ IDEA can notify you right away whether or not the code pattern can be found in the specified scope. 

![Structural Search dialog: module scope](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_no_match_in_scope.png)
  6. Check the result in the Find tool window. 

![Find tool window: final field search result](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_final_field_result.png)



With the structural search, we can conduct some interesting searches. Let's choose another existing template (method calls) as our example.

### Use an existing template (method calls)

  1. In the Structural Search dialog, click ![the Tools icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) and select Existing Templates.

  2. Open the list of the existing templates, and select the method calls template under the Expressions node. 

![Existing Templates dialog: method calls](https://resources.jetbrains.com/help/img/idea/2025.3/method_calls_template.png)
  3. If we run the search now, we'll end up with results that include all the method call in our code. So, we should alter our template a bit and use modifiers to be more specific of what we are looking for. Let's add a modifier `Text` and define a method called `print`. We'll look for calls to a method called `print`.

  4. We can add a regex expression, for example, find all the calls to methods that contain `print`. To do that let's switch `print` to `print.*`. 

Now the result of our search will include not only print, but also `println` and `printf`.

  5. Let's change our search pattern so that the result will only display methods that take only a single parameter. Click the `$Parameter$` variable and add the count modifier `min=1` `max=1`. 

![Add the count modifier for parameter](https://resources.jetbrains.com/help/img/idea/2025.3/parameter_filter.png)

In this case, we'll have fewer search results.




Let's assume we're doing this search to replace all these method calls with logging calls instead of `System.out`. The logging methods take only strings and no other types.

First, let's find methods that pass the string.

  1. In the Structural Search dialog, add a modifier Type for the `$Parameter$` variable. 

![Add type modifier string](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_param_string.png)
  2. Click Search. As a result, we see a list of print methods that take only literal string or a variable of type `String`. 

![the Find tool window: results](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_result_param_string.png)



Now let's do our replacement.

### Replace code

  1. Use the Search Everywhere window to access Structural Replace.

  2. In the Structural Replace dialog in the Replace Template add code with which you want to replace our search results. In our case it is `java.util.logging.Logger.getLogger(this.getClass().getName()).fine($Parameter$)`

![The Structural Replace dialog: replace pattern](https://resources.jetbrains.com/help/img/idea/2025.3/replace_pattern.png)

Click Find.

  3. Check the results in the Find tool window and use the replace options to replace all of the results or just the selected ones. 

![the Find tool window: replace results](https://resources.jetbrains.com/help/img/idea/2025.3/find_tool_window_replace.png)

As you can see the code was changed.

![the replace results](https://resources.jetbrains.com/help/img/idea/2025.3/replace_results.png)



We can save this template to refer to it later if we need.

### Save the modified template

  1. In the Structural Replace dialog, click ![Tools](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg).

  2. In the list that opens, select Save Template.

  3. Let's add the name of our template (print String calls) and click OK. 

The template is saved under the User Defined node in the Existing Templates dialog.

![the saved template](https://resources.jetbrains.com/help/img/idea/2025.3/saved_template.png)

While in the Structural Replace dialog, we can click ![the Search icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.search.svg) to check out the history of your recent searches and quickly rerun any of them.

![the recent entries](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_recent_search.png)



We can also use our template as an inspection, so when we come across the same code, we'll see a warning and can quickly replace the code.

### Create a custom inspection

  1. In the Find tool window, when you get the results for the replace pattern, click Create Inspection from Template.

  2. In the dialog that opens, let's add the name for our template `print String calls`. 

![the Structural Search Inspection dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_inspection_dialog.png)

If you want you can add a tooltip and click OK.

  3. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | Inspections.

  4. On the Inspections page, open the Structural search node to locate the created inspection. 

![the Inspections settings: Structural search inspection](https://resources.jetbrains.com/help/img/idea/2025.3/inspections_page_ssr_inspection.png)

Now we can quickly fix the code in the editor or use the Problems view where we can check a warning with the suggestion to replace it with the new code.

![the Problems view](https://resources.jetbrains.com/help/img/idea/2025.3/problems_tool_window_replace.png)



We can add a custom structural search inspection right from the inspections settings.

### Create a custom inspection from the inspections settings

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | Inspections.

  2. On the Inspections page, select the Structural search node and click ![Add structural search replace inspection](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg). We can base our inspection either on a search template or a replace template. Let's select Add Replace Template.

  3. In the Structural Replace dialog, let's slightly change our search pattern. Let's change the `Type` modifier for our `$Parameter$` variable to `int`.

  4. In the replace pattern let's tweak our code. `java.util.logging.Logger.getLogger(this.getClass().getName()).fine(String.valueOf($Parameter$))`

![Change pattern](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_change_to_int_pattern.png)
  5. In the dialog that opens let's add a name of our inspection `print int calls` and click OK. 

![Inspection name](https://resources.jetbrains.com/help/img/idea/2025.3/print_int_calls.png)

The new inspection is added under the Structural search, and we can run it to search for instances that print an integer. When code like this is found, we can replace it with the logger call and convert the found parameter into a string.




We can run our inspection separately using its name.

### Run the structural search inspection

  1. Press `Ctrl+Alt+Shift+I` or go to Code | Analyze Code | Run Inspection by Name in the main menu.

  2. In the dialog that opens, let's enter the name of our inspection `print String calls`. 

![Enter inspection name](https://resources.jetbrains.com/help/img/idea/2025.3/inspection_name.png)
  3. In the Run 'print String calls' dialog, let's leave default options and click OK. 

![Inspection scope](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_inspection_scope.png)
  4. We can review our results in the Inspection results tool window. 

![Inspection results](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_inspection_results.png)



26 May 2024

[Structural search and replace examples](structural-search-and-replace-examples.html)[Structural search and replace dialogs](structural-search-and-replace-dialogs.html)
