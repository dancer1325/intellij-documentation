[//]: # (Source: https://www.jetbrains.com/help/idea/xpath-expression-evaluation.html)
[//]: # (Downloaded: 2025-12-17 20:07:45)

# XPath expression evaluation

An XPath expression needs evaluation to test it before using in program code or XSLT scripts or before making structured queries against XML documents.

IntelliJ IDEA lets you evaluate XPath expressions in two modes:

  * In the Simple mode, you can enter simple one-line expressions that don't require any customization of namespace prefixes. This mode does not let you configure Context settings or use predefined variables.

  * In the Advanced mode, you can conveniently edit long expressions in a multi-line mode and edit the XPath context.




Some error checks and XPath inspections also provide quick-fixes for detected problems, for example, the possibility to map an unresolved namespace-prefix to a URI by intention.

### Enable the XPathView + XSLT plugin

This functionality relies on the [XPathView + XSLT](https://plugins.jetbrains.com/plugin/12478-xpathview--xslt) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The XPathView + XSLT plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the XPathView + XSLT plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the XPathView + XSLT plugin, and select the checkbox next to the plugin name.




### Evaluate an XPath expression

  1. Select Evaluate XPath from the context menu of the active editor tab or go to Edit | Find | Evaluate XPath. The Evaluate XPath Expression dialog opens.

  2. To toggle the evaluation mode, click the Advanced/Simple button. In either mode, the dialog features a history of the recently evaluated expressions, completion, syntax-checking and highlighting, as well as some semantic error checking of the entered expression. Semantic checks include validation of used namespace prefixes, useless XPath expressions (for example, `@comment()`) and node tests for element/attribute names that don't occur in the context document and would not be successfully matched.

  3. To browse through the history of expressions:

     * In the Simple mode, the last recently used expressions can be selected from the drop-down list.

     * In the Advanced mode, use ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg)/![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg) or press `Alt+Up`/`Alt+Down`.

  4. To reconfigure the XPath context, click Edit Context. In the dialog that opens, assign custom prefixes to the namespace URIs that are used in the context document and define variables to use in queries for repeating expressions.

It can be useful to assign a shorter prefix, resolve prefix clashes or to actually define a prefix for the default namespace. This can be essential because XPath does not automatically match elements in the default namespace without specifying a prefix for the element to be matched. edit namespaces and their prefixes and

Each variable in the table can be assigned an expression that will be evaluated once when the query is executed. The resulting value is then available for multiple use at no additional computational cost.

  5. Optionally:

     * Select the Highlight results checkbox to highlight the matched nodes in the current editor. Matched nodes that don't belong to the current editor (may happen by using the `document()` function) are not highlighted. It's recommended to display such cross-document results in the Find Usages tool window.

     * Select the Show results in Usage View checkbox to show all matched nodes in the Find Usages tool window. Select the Open in new tab checkbox to open the result in a new tab instead of reusing the last one.




06 September 2024

[XPath and XSLT support](xpath-and-xslt-support.html)[XPath search](xpath-search.html)
