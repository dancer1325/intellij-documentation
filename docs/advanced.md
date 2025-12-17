[//]: # (Source: https://www.jetbrains.com/help/idea/advanced.html)
[//]: # (Downloaded: 2025-12-17 19:17:59)

# Advanced

Use this page to specify different names for the base-annotations to be used. This helps avoid any dependencies on foreign code where it is not desired or possible. The custom annotations should provide the same properties as the original ones, i.e. `value` for all of them and an optional (default = "") `prefix` and `suffix` for the `@Language` replacement.

Also configure the runtime checks to be generated for the `@Pattern` validation.

Item| Description  
---|---  
Annotation Classes| In this area, specify the classes that implement [annotations](annotating-source-code.html) of the following types: 

  * Language annotations
  * Pattern annotations
  * Substitution annotations

Type the class names, possibly using code completion. If necessary, use ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the Select Class dialog, where you can locate the desired class in the project tree view. Alternatively, switch to the Search by Name tab and start typing the class name. As you type, the list of available classes narrows down to match your entry.  
Runtime Pattern Validation| In this area, configure the runtime checks to be generated for the `@Pattern` validation. The available options are: 

  * No runtime instrumentation \- if this option is selected, no checks will be inserted and any compiled class files will be affected.
  * Instrument with assertions \- if this option is selected, pattern-validation is controlled with the `-ea` JVM switch and throws `AssertionError`. Selecting this option is recommended due to the potentially negative impact on the performance for methods that are invoked very often.
  * Instrument with IllegalArgumentException \- select this option to have the same result as when the `@NotNull` instrumentation of IntelliJ IDEA is used.

  
Performance| Click one of the radio buttons in this area to select the level of analysis and performance of the language injections resolution procedure. 

  * Do not analyze (fast) \- if this option is selected, IntelliJ IDEA does not analyze injections. Selecting the Do not analyze option significantly improves performance.
  * Analyze references \- if this option is selected, IntelliJ IDEA attempts to recognize injections introduced through variables.
  * Look for variable assignments \- if this option is selected, IntelliJ IDEA does not perform the dataflow analysis to detect the substitution strings, but looks for variable assignments only.
  * Use dataflow analysis (slow) \- if this option box is selected, IntelliJ IDEA applies [dataflow analysis](analyzing-data-flow.html) to language injections.

  
Convert undefined operands to text in concatenation| If this checkbox is selected, IntelliJ IDEA inserts an injected operand as a literal, if its type is not recognized.  
Add @Language annotation or comment if needed| This checkbox enables/disables adding annotations or comments.  
  
28 June 2024

[Language Injection Settings dialog: XML Tag Injection](language-injection-settings-dialog-xml-tag-injection.html)[Reader mode](reader-mode.html)
