[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-xml.html)
[//]: # (Downloaded: 2025-12-17 20:07:36)

## Import XML namespaces

If you use a tag or an attribute from a namespace that is not bound, IntelliJ IDEA detects the problem and shows a tooltip:

![Tooltip: Reference to an unbound namespace](https://resources.jetbrains.com/help/img/idea/2025.3/import_unbound_namespace_tooltip.png)

To solve the problem, use the quick-fix that IntelliJ IDEA suggests.

  * Press `Alt+Enter`. If there are multiple choices, select the desired namespace from the list. 

  * Alternatively, hover over the problem and click Create namespace declaration in the popup that opens. If there are multiple choices, select the desired namespace from the list.




Depending on the file type, IntelliJ IDEA creates a namespace declaration, or a taglib.
