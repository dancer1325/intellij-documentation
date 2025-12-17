[//]: # (Source: https://www.jetbrains.com/help/idea/xpath-expression-generation.html)
[//]: # (Downloaded: 2025-12-17 20:07:46)

# XPath expression generation

### Enable the XPathView + XSLT plugin

This functionality relies on the [XPathView + XSLT](https://plugins.jetbrains.com/plugin/12478-xpathview--xslt) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The XPathView + XSLT plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the XPathView + XSLT plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the XPathView + XSLT plugin, and select the checkbox next to the plugin name.




This action computes a unique XPath expression that matches the currently selected node in the document. The action is available from the main menu (View | Unique Path) and the editor context menu (Show Unique XPath). The action is only enabled when the caret is placed on an element that a useful expression can be generated for. 

The generated expression in the popup can be selected and copied into the clipboard for further use.

If a simple XPath expression like `/root/something/else` doesn't produce a unique result, the action has two strategies to make it unique:

  * If the non-unique node is an element, the action looks for attributes with the name `id`, `name`, and attributes that are of ID type, as defined by the document's DTD or XML Schema. For example: `/root/something[@id="foo"]/else`

  * For nodes other than elements (comments, processing instructions), or if the above rule doesn't produce a unique result, the index of the node inside its parent is appended. For example: `/root/something/else[2]`




06 September 2024

[XPath search](xpath-search.html)[XPathView + XSLT plugin settings](xpath-plugin-settings.html)
