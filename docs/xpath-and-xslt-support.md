[//]: # (Source: https://www.jetbrains.com/help/idea/xpath-and-xslt-support.html)
[//]: # (Downloaded: 2025-12-17 20:07:44)

# XPath and XSLT support

  * XSLT support is available in all XML files that declare the XSLT-Namespace `http://www.w3.org/1999/XSL/Transform` on their root element.

  * IntelliJ IDEA supports XSLT versions 1.0 and 2.0, XPath versions 1.0 and 2.0.




Coding assistance is available in IntelliJ IDEA for XSLT 1.0, 2.0, and 3.0. However, to use transformations with XSLT 2.0 or 3.0, a processor supporting XSLT 2.0 or XSLT 3.0 (for example, Saxon 9-HE) should be added to the classpath of a module that is used to run a Style Sheet, and placed in front of JDK. See [Module dependencies](working-with-module-dependencies.html).

IntelliJ IDEA lets you evaluate expressions against the currently focused document, including support for the `document()` function to make cross-document queries. You can also evaluate an expression against multiple XML documents in the Find in Files style using the [Find by XPath](xpath-search.html) action.

You can configure to highlight matching expressions in the current editor or to show a list of matching lines in the [Find tool window](find-tool-window.html). Editing XPath expressions is enhanced by on-the-fly error-checking including a set of customizable XPath inspections and a wide range of code completion suggestions.

IntelliJ IDEA also lets you display a unique XPath expression for a selected element in the editor by choosing View | Unique XPath from the main menu.

XSLT support is not limited to XPath expressions, it also supports a wide range of XSLT constructs, like checking the existence of templates that are called via `xsl:call-template` and their parameters, refactoring and navigation enhancements. The bundled [XSLT Debugger](https://plugins.jetbrains.com/plugin/1818-xslt-debugger) plugin allows you to debug XSLT stylesheets. 

### Enable the XPathView + XSLT plugin

This functionality relies on the [XPathView + XSLT](https://plugins.jetbrains.com/plugin/12478-xpathview--xslt) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The XPathView + XSLT plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the XPathView + XSLT plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the XPathView + XSLT plugin, and select the checkbox next to the plugin name.




20 October 2025

[XML refactorings](xml-refactorings.html)[XPath expression evaluation](xpath-expression-evaluation.html)
