[//]: # (Source: https://www.jetbrains.com/help/idea/components-treeview.html)
[//]: # (Downloaded: 2025-12-17 19:21:29)

# Component Tree

### Install the Swing UI Designer plugin

This functionality relies on the [Swing UI Designer](https://plugins.jetbrains.com/plugin/25304-swing-ui-designer) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Swing UI Designer plugin, and click Install (restart the IDE if prompted).




The Component Tree is [a section of a form](design-gui-using-swing.html#sections-of-a-form) that displays the components contained in the design form and enables you to navigate to and select one or more components. Selection of one or more components here is reflected in parallel on the design form and vice versa.

![The component tree section of a form](https://resources.jetbrains.com/help/img/idea/2025.3/component_tree_section.png)

The Component Tree hierarchy represents containment. Expandable nodes represent some type of container. Sub-nodes of containers represent UI components (including nested containers). The root node represents the Form, which is, in effect, the top-level container for the GUI you are building with the UI Designer.

When you create a new Form, a JPanel component is automatically added to the form workspace, and it appears as a child of the Form in the Component Tree. This JPanel is the top of the UI component hierarchy (in the Java sense) for the current Form. All other Swing or other UI components are contained within it. It is also possible to move components from one container to another using a drag-and-drop operation in the Component Tree.

15 October 2024

[Form workspace](form-workspace.html)[ Property inspector](inspector.html)
