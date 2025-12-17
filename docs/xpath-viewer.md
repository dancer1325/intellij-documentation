[//]: # (Source: https://www.jetbrains.com/help/idea/xpath-viewer.html)
[//]: # (Downloaded: 2025-12-17 20:07:50)

# XPath Viewer

This page appears if [XPathView + XSLT](xpath-and-xslt-support.html) plugin is enabled. In this page, configure the IntelliJ IDEA behaviour during interactive execution of XPath expressions.

### Enable the XPathView + XSLT plugin

This functionality relies on the [XPathView + XSLT](https://plugins.jetbrains.com/plugin/12478-xpathview--xslt) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The XPathView + XSLT plugin is available by default only in IntelliJ IDEA with the Ultimate subscription. For IntelliJ IDEA, you need to install the XPathView + XSLT plugin as described in [Install plugins](managing-plugins.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the XPathView + XSLT plugin, and select the checkbox next to the plugin name.




Item| Description  
---|---  
Scroll first hit into visible area| Select this checkbox to have the editor automatically scroll to the first XPath match.  
Use node at cursor as context node| Select this checkbox to have the entered XPath expression use the currently selected node (tag/attribute/pi, and so on) as its context node and evaluate the expression relatively to this node.  
Highlight only start tag instead of whole tag content| Do one of the following:

  * Select this checkbox to have only the name of a matching tag highlighted.
  * Clear this checkbox to have the entire content of a matching tag highlighted.

  
Add error stripe markers for each result| Select this checkbox to have each match supplied with an error stripe marker which can be quickly navigated to. The tooltip of each marker shows the matched content.  
Colors| In this area, configure color indication during execution of XPath expressions. Clicking on the color box will open the Select Color dialog in which you can modify the current color indication.

  * Highlight Color: select the color to indicate XPath matches in the editor.
  * Context Node Color: select the color to indicate the current context node.

  
  
11 February 2024

[Vagrant](vagrant.html)[Web Services](web-services-settings.html)
