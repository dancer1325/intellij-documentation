[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-structure-and-hierarchy-of-the-source-code.html)
[//]: # (Downloaded: 2025-12-17 20:06:29)

## Analyzing Code Hierarchies

  * Type hierarchies show parent and child classes of a class.

  * Method hierarchies show subclasses where the method overrides the selected one as well as superclasses or interfaces where the selected method gets overridden.

In the hierarchy tree, IntelliJ IDEA displays ![the method should be defined icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.hierarchy.shouldDefineMethod.svg) to indicate subclasses that are not abstract but don't have the method defined in them. When a method is not defined in a class, but is defined in the superclass, IntelliJ IDEA displays ![the method not defined icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.hierarchy.methodNotDefined.svg).

  * Call hierarchies show callers (supertypes) or callees (subtypes) of a method. 

If you invoke the call hierarchy on a field, it will show you the list of the methods where the selected field is used.




When built, a hierarchy can be immediately viewed and examined in the Hierarchy tool window. By default, every new built hierarchy overwrites the contents of the current tab. You can retain the current tab and have the next hierarchy built in a new one.

### Build a type hierarchy

  1. Select the desired class in the Project tool window or open it in the editor. 

  2. In the main menu, go to Navigate | Type Hierarchy or just press `Ctrl+H`. 

![Class hierarchy shown in the Hierarchy Tool Window](https://resources.jetbrains.com/help/img/idea/2025.3/java_type_hierarchy.png)



Different colors of elements stand for different scopes to which these files belong. For example, green by default is used for tests. For more information, refer to [Associate scopes with colors](configuring-scopes-and-file-colors.html#associate-file-color-with-a-scope).

### Build a method hierarchy

  1. Open the file in the editor and place the caret at the declaration of the desired method.

Alternatively, select the desired method in the Project tool window.

  2. Go to Navigate | Method Hierarchy or press `Ctrl+Shift+H`.




### Build a call hierarchy

  1. Open a file in the editor and place the caret at the declaration or usage of the desired method or a field.

Alternatively, select the desired method or the field in the Project tool window.

  2. In the main menu, go to Navigate | Call Hierarchy or press `Ctrl+Alt+H`. 




### Retain a hierarchy tab

  * In the Hierarchy tool window, click the Pin Tab button ![Pin button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.pin.svg) on the toolbar.



