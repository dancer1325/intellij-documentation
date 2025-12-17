[//]: # (Source: https://www.jetbrains.com/help/idea/palette.html)
[//]: # (Downloaded: 2025-12-17 19:33:46)

# Palette

### Install the Swing UI Designer plugin

This functionality relies on the [Swing UI Designer](https://plugins.jetbrains.com/plugin/25304-swing-ui-designer) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Swing UI Designer plugin, and click Install (restart the IDE if prompted).




The Palette is [a section of a form](design-gui-using-swing.html#sections-of-a-form) that appears by default on the right side of the frame next to the form workspace. It contains UI components which you can visually place on a Form. The default Group of the Palette contains a set of Swing user interface components that you can arrange on forms as needed. The Swing group also has horizontal and vertical Spacers that you can place on the form to define space between components. (These can behave differently depending on the setting in the Layout Manager property of the container into which a spacer is placed.) You can customize the Palette to contain additional groups, as well as your own or third-party GUI components.

The context menu of the Palette tool window provides functions for managing components and groupings. Two groups are present by default:

  * Swing: contains components from the Swing component library.

  * Palette: contains a single component labeled _Non-Palette component_. When you select this _component_ and add it to a Form, a dialog appears in which you can select any component class accessible to your project, or any other existing Form. This is useful in cases where you want to use a component without adding it to the Palette.


![The palette section of a form](https://resources.jetbrains.com/help/img/idea/2025.3/uid_palette.png)

If you have your own custom components, or if you reuse components from third-party libraries, you can add them to the Palette via the context menu, which also enables you to add component groups.

15 October 2024

[Component properties](components-properties.html)[Add/Edit palette component](add-edit-palette-component.html)
