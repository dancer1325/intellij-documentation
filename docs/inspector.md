[//]: # (Source: https://www.jetbrains.com/help/idea/inspector.html)
[//]: # (Downloaded: 2025-12-17 19:29:33)

#  Property inspector

### Install the Swing UI Designer plugin

This functionality relies on the [Swing UI Designer](https://plugins.jetbrains.com/plugin/25304-swing-ui-designer) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Swing UI Designer plugin, and click Install (restart the IDE if prompted).




The property inspector is [a section of a form](design-gui-using-swing.html#sections-of-a-form) that shows properties for the component currently selected in the form workspace, or the form itself if no components exist or none are selected.

In this section you will find information about the groups of properties, context menu commands, and types of editors.

The property inspector has two groups of properties, as shown in the following figure:

![The property inspector section of a form](https://resources.jetbrains.com/help/img/idea/2025.3/property_inspector.png)

Item| Description  
---|---  
Upper group| The shaded properties at the top of the proerpty inspector are proprietary to IntelliJ IDEA; they are mainly used to control the layout constraints of the components for the given layout. These properties are layout-specific and depend on the layout of the container where the component is placed.  
Lower group| This group is not shaded and contains properties of the selected Swing component. There are two levels of properties: _Basic_ and _Expert_. The Expert level can be toggled on and off using the Show Expert Properties checkbox in the bottom line of the property inspector. For more information, refer to [Sun documentation for the Swing libraries](http://java.sun.com/javase/6/docs/technotes/guides/swing/index.html).  
  
The context menu of each property provides the following commands:

Item| Keyboard Shortcut| Description  
---|---|---  
Quick Javadoc| `Ctrl+Q`| Opens related API documentation for the selected property, provided that the necessary paths are added to the API docs in the Project Settings.  
Jump to Source| `F4`| Opens in the editor the source code of the class that contains the selected property.  
Restore Default Value| | This command is enabled for the modified properties only.  
  
Several types of property editors appear in the Value column of the inspector:

  * Text field: Type a value.

  * Pick list: Pick a value from a drop-down list of valid choices.

  * Checkbox: Set value for Boolean type properties.

  * Dialog: Presents an ellipsis button which opens a dialog.




15 October 2024

[Component Tree](components-treeview.html)[Component properties](components-properties.html)
