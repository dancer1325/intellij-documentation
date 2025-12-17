[//]: # (Source: https://www.jetbrains.com/help/idea/add-edit-palette-component.html)
[//]: # (Downloaded: 2025-12-17 19:17:46)

# Add/Edit palette component

GUI Designer Palette | context menu | Add / Edit Component

### Install the Swing UI Designer plugin

This functionality relies on the [Swing UI Designer](https://plugins.jetbrains.com/plugin/25304-swing-ui-designer) plugin, which you need to install and enable. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Swing UI Designer plugin, and click Install (restart the IDE if prompted).




Use this dialog to create a new component in the [Palette](palette.html) or change an existing one.

Item| Description  
---|---  
Class| Click this radio-button to add a component from a class library. You can enter a fully qualified class name in the text field or click the ellipsis button and select a class from the libraries, or project. Note that code completion is available in the text field.  
Form| Add an existing GUI form. You can enter a fully qualified form name in the text field, or click the ellipsis button and select a form from the libraries, or project.  
Icon| Specify the fully qualified name of the icon file, or click the ellipsis button and select an icon file from the libraries, or project.  
Group| Select the target group where the new component will be added. This field is available for the Add Component dialog only.  
Horizontal / Vertical Size Policy| The sizing policies define the behavior of the component when its parent container is being resized.  
Can shrink| If this option is checked, the size of the component can be reduced when the container is resized.  
Can grow| If this option is checked, the size of the component can increase when the container is resized.  
Want grow| If this option is checked, the size of the component can increase when the container is resized. This option has a higher priority when competing with the cells of the other components.  
Is container| If this option is checked, the component can accommodate nested components and acquire some properties that pertain to the containers.  
Create binding automatically| If this option is checked, the field for the component is automatically added to the bound class.  
Can have attached label| If this option is checked, the component of this type appears in the `labelFor` field of a `JLabel` component in the [property inspector](inspector.html). It is important to note that the Can have attached label option affects all components of this type on a GUI form. For example, if you check this option for `JButton` and `JCheckBox` Palette components, all instances of these components (already existing and newly added) appear in the `labelFor` field: ![The labelFor field of a JLabel component](https://resources.jetbrains.com/help/img/idea/2025.3/labelFor.png)  
  
15 October 2024

[Palette](palette.html)[Web development](web-development.html)
