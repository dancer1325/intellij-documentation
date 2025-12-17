[//]: # (Source: https://www.jetbrains.com/help/idea/xpath-search.html)
[//]: # (Downloaded: 2025-12-17 20:07:49)

# XPath search

IntelliJ IDEA lets you use XPath 3.0 to find specific XML nodes in XML files in your current project, directory, or within a custom scope.

When you compose an XPath expression, IntelliJ IDEA provides code completion for XPath axes and checks the expression syntax. It also provides XPath syntax highlighting, which can be customized in Settings | Editor | Color Scheme | XPath.

### Enable the XPathView + XSLT plugin

This functionality relies on the [XPathView + XSLT](https://plugins.jetbrains.com/plugin/12478-xpathview--xslt) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The XPathView + XSLT plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the XPathView + XSLT plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the XPathView + XSLT plugin, and select the checkbox next to the plugin name.




### Search in XML files

  1. In the main menu, go to Edit | Find | Find by XPath. The Find by XPath Expression dialog opens.

  2. Type an XPath expression.

For example, the following expression:

//application[@title="BestApp"]/descendant::resource 

will search for `resource` tags that are descendants of an `application` tag that has an attribute `title` with the value `BestApp`.

  3. Choose the scope for the search.

If you select Directory and specify a path to a directory, you can also select the Recursively checkbox to search for nodes in all subdirectories.

The XPath search results are displayed in the [Find](find-tool-window.html) tool window.




11 October 2024

[XPath expression evaluation](xpath-expression-evaluation.html)[XPath expression generation](xpath-expression-generation.html)
