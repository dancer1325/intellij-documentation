[//]: # (Source: https://www.jetbrains.com/help/idea/structural-search-and-replace.html)
[//]: # (Downloaded: 2025-12-17 20:03:28)

# Structural search and replace

A conventional search process does not take into account the syntax and semantics of the source code. Even if you use regular expressions, IntelliJ IDEA still treats your code as a regular text. The structural search and replace (SSR) actions let you search for a particular code pattern or grammatical construct in your code considering your code structure.

IntelliJ IDEA finds and replaces fragments of source code, based on the [search templates](search-templates.html) that you create and [conditions](search-templates.html#ssr_filters) you apply.

Currently, IntelliJ IDEA supports the structural search and replace for Java, Kotlin, Scala and Groovy.

### Search for a target structurally

  1. In the main menu, go to Edit | Find | Search Structurally to open the Structural Search dialog.

To quickly switch to the Structural Replace dialog, click ![the Switch to Replace icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg).

  2. In the Structural Search dialog, do one of the following:

     * Create a template from scratch: select Draft Template from the list of templates and enter the code template (for example, `$variable$` to represent your code) in the editor area.

To save your custom template for future use, click the Save Template icon (![the Save Template button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.save.svg)) on the dialog toolbar. You can also choose to save the template as an inspection.

![Structural Search dialog](https://resources.jetbrains.com/help/img/idea/2025.3/structural_search_dialog.png)

IntelliJ IDEA adds the created template to the Recent node in the template list.

     * Use one of the existing templates to act as a prototype: select the necessary template from the list of available existing templates.

For example, you have the following fields in your code:

public class MainActivity { public static final String this_is_wrong = "Hello"; public static final String THIS_IS_CORRECT = "world"; } 

Let's find a certain field in the class.

From the list of existing templates, click Java and open the Class-based node (since we need fields in the class), so the fields of the class template would be our target. 

![the existing templates list](https://resources.jetbrains.com/help/img/idea/2025.3/existing_templates.png)

Click Find to search for these constructions in the entire project.

IntelliJ IDEA instantly highlights the found code occurrences in the editor.

  3. The Structural Search dialog shows the selected template and the values of its filters. You can edit existing filters or add new [conditions](search-templates.html#ssr_filters), such as regular expressions or [script constraints](search-templates.html#script_constraints). Place the caret on a code variable and use the filter area to manage its filters.

![the Edit filters](https://resources.jetbrains.com/help/img/idea/2025.3/Edit_filters.png)
  4. In this example, add a Text modifier for the `$Field$` variable.

  5. For the Text modifier, enter the following regular expression:

\b[A-Z].*?\b 

![Add a regular expression in the filter dialog](https://resources.jetbrains.com/help/img/idea/2025.3/add_filter_text_regex_ssr.png)

In this case, when you select the Match case checkbox in the Structural Search dialog, IntelliJ IDEA searches only for fields with uppercase characters in the first field.

There are also additional options available depending on the selected language.

For example, review the following options:

     * Language: use the list to select which file types to include in the search. In this case, it is Java. 

     * Target: use the list to select what item to search for. In this case, it is `Field`. 

![Search target](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_search_target.png)
     * Recursive: if selected, IntelliJ IDEA performs a recursive search, and all nested items are included in the results. For example, when you search for a method call with Recursive enabled, IntelliJ IDEA finds nested calls in `foo(foo(foo()))`. With Recursive disabled, only the outer call is found.

     * Injected code: if selected, injected code such as JavaScript in HTML or SQL in Java is included in the search.

     * Match case: if selected, the search results match the case of the search target.

  6. Specify the search scope: a project, module, directory, or a custom scope.

  7. Click Find.

IntelliJ IDEA shows the results in the Find tool window.

![Find tool window results](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_find_tool_window_results.png)

You can add the new search template to [structural search inspections](creating-custom-inspections.html) as a custom template. To do this, click Create Inspection from Template in the Find tool window. You can then reuse it to inspect your code.

In some cases, inspections can replace structural search and replace. For example, replacing classes with interfaces through structural search does not update usages, so you would need to run search and replace multiple times. In this case, you can use the abstract class may be interface inspection, which also updates usages of the abstract class.




### Replace a target structurally

  1. In the main menu, go to Edit | Find | Replace Structurally.

  2. In the Replace Structurally dialog, add new or [existing templates](#existing_templates) to the search and replace template areas. You can save the replace template the same way as the [search](#ws_save_template) one.

  3. If you need to add a filter for the variable in the replace template, place the caret at the variable of interest and use the filter area to manage filters.

  4. In the filter area, depending on what you chose as a [filter](search-templates.html#ssr_filters), specify the condition.

For example, let's take a variable `$Field$` that we [searched for](#field_condition) and add a condition to replace the found template with the lowercase characters.

Let's call our variable `$Field2$` and add the following filter script which basically is a Groovy script: `Field.name.toLowerCase()`.

![the Replace template](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_replace_pattern.png)
  5. To narrow down your replace results, select the following options:

     * Shorten fully-qualified names \- replaces fully qualified class names with short names and imports.

     * Reformat \- automatically formats the replaced code.

     * Use static import \- uses static import in replacement when possible. For example, a method call to a static method `Math.abs(i)` becomes `abs(i)` if this option is selected. 

After specifying the necessary options, click Find. IntelliJ IDEA displays the results in the Find tool window.

  6. In the Find tool window, you can work with the results further, replacing found items one by one, or all of them at once, or previewing your potential changes.

You can also add the replace template to the [structural search inspections](creating-custom-inspections.html) and use it as a quick-fix for your code.

![the Find tool window             with the Replace preview](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_replace_preview.png)

As a result of our replacement, the uppercase characters were switched to lowercase.

![the Replace result](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_replace_result.png)



### Share search templates

You can share a search template with your peers by exporting or importing it.

  1. In the Structural Search dialog (Edit | Find | Search Structurally), [create a new search template or use the existing one](#to_search_structurally).

  2. To export a template, click ![the Export Template to Clipboard icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.export.svg). IntelliJ IDEA adds the XML representation of the template to a clipboard (press `Ctrl+Shift+V` to see the clipboard's content). You can share this representation with other developers in chat, email, or a forum.

To import a template, copy (`Ctrl+C`) the shared XML code from anywhere (email, chat, or a forum) and in the Structural Search dialog, click ![the Import Template from Clipboard icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.import.svg). IntelliJ IDEA takes the XML code representation and converts it into a template including variables and a scope if it is present.




04 December 2025

[Search for usages](find-highlight-usages.html)[Search templates, modifiers, and script constraints](search-templates.html)
