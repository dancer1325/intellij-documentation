[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-structural-search-and-replace-in-kotlin.html)
[//]: # (Downloaded: 2025-12-17 20:04:49)

# Tutorial: Structural search and replace in Kotlin

Structural search and replace is a powerful tool that can search for a specific pattern in code and replace it in an automated way.

In this tutorial we will get acquainted with templates and filters, modify a predefined template, and then create a code inspection based on it.

The functionality covered in this tutorial is by no means the exhaustive list of what Structural Search and Replace can do. Our goal is to get you started. After that, you can explore various templates, filters, and options and combine them to create your own specific searches.

For the tutorial, we will use the following code:

class Point constructor(locationX: Int, locationY: Int) { var x: Int = locationX var y: Int = locationY } open class OpenClass { open var openProperty = 0 open fun display() { println("Some text") print("More text") print(0) } } 

### Open the Search Structurally dialog

  * In the main menu, go to Edit | Find | Search Structurally.




### Use an existing template (property declaration)

  1. In the Structural Search dialog, select Kotlin from the list on the left.

  2. Expand the Class-based node and click All vars of a class. 

  3. Make sure that Kotlin is selected as Language. This makes the search only apply to Kotlin files. 

![Search for Kotlin files only](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-vals-vars.png)
  4. Click Find to run the search. As the result, in the Find tool window, IntelliJ IDEA shows all the properties declared in Kotlin classes.

![Matches found in project files](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-vals-vars-result.png)



### Rerun

  * While in the Structural Search dialog, expand the Recent node to browse the history of your recent searches and quickly rerun any of them.




Now, let's return to our structural search dialog to alter the predefined template a bit.

### Alter a predefined template

  1. In the Structural Search dialog, let's update our template to only search for open properties by adding `open` before the `$Field$` variable.

![Change class find template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-all-open-fields.png)

If we change the scope, IntelliJ IDEA will notify you right away whether the code pattern can be found in the specified scope.

  2. Click Find and check the result in the Find tool window.

![Results for all open fields](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-all-open-fields-result.png)

As you can see, the search used the filter this time and only shows the open properties now.




With Structural Search, we can run some interesting searches. Let's choose another existing template (Method calls) as our example. Assume we're doing this search to replace all `print` statements with logging calls and exclude all calls that do not have a `String` as the argument.

### Replace function calls

  1. In the main menu, go to Edit | Find | Replace Structurally.

  2. Under the Kotlin | Expressions node, select Method calls. 

![Kotlin method calls template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-function-calls.png)
  3. If we run the search now, we'll end up with results that include all the function calls in the code. So, we should alter our template a bit and use filters to be more specific about what we are looking for.

Place the caret at `$MethodCall$` and in the right-hand pane, click Add modifier. Add a Text filter with the value of `print.*`.

Using `print` without the wildcard would only find calls to functions named exactly `print`. The regex will ensure that the result will include calls to all functions that have `print` in their name, for example, `println`.

![Add a text filter to the search template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-replace-1.png)
  4. Place the caret at `$Before$` and in the right-hand pane, make sure that the only modifier is `Count=[0,1]`.

  5. Place the caret at `$Parameter$` and in the right-hand pane, click ![the Plus icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg). Add a Type filter with the value of `String`.

![Add a type filter to the search template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-replace-2.png)
  6. In the Replace template area, add the replacement code: `java.util.logging.Logger.getLogger(this.javaClass.getName()).fine($Parameter$)`

![Add the replacement code](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-replace-3.png)
  7. Check the results in the Find tool window and use the replace options to select which of the results you want to replace.

![Results for the replacement template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-replace-4.png)



We can save this template for later use if we need.

### Save template

  1. In the Structural Replace dialog, click ![the Tools button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg).

  2. In the list that opens, select Save current template.

  3. Specify the name for the template and click OK.

![Save replacement template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-save-template-2.png)



The template is saved under the Saved Templates node.

![The list of user-defined templates](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-save-template-3.png)

We can also use our template as an inspection, so when we come across the same code, we'll see a warning and can quickly replace the code.

### Create a custom inspection

  1. In the Find tool window, where you get the results for the replace pattern, click Create Inspection from Template.

![Create a new inspection from the replace template](https://resources.jetbrains.com/help/img/idea/2025.3/kotlin-ssr-create-inspection-1.png)
  2. In the dialog that opens, add the name for the inspection. Optionally, add a tooltip (provides a more detailed description of the problem on hovering over the highlighted code). Click OK.




The newly created inspection appears under the Structural search node in Settings | Editor | Inspections.

To quickly run an inspection, select Code | Analyze Code | Run Inspection by Name. from the main menu or press `Ctrl+Alt+Shift+I`) and enter the name of the inspection.

11 October 2024

[Tutorial: Test-driven development with Kotlin](tdd-with-kotlin.html)[Run/Debug Configuration: Kotlin](run-debug-configuration-kotlin.html)
