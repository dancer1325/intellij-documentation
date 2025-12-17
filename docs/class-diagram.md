[//]: # (Source: https://www.jetbrains.com/help/idea/class-diagram.html)
[//]: # (Downloaded: 2025-12-17 19:19:58)

## Analyze class diagram

You can press `Ctrl+F12` on the element to view a list of diagram elements and navigate between them.

To see the list of methods, fields, and other code elements, select the appropriate [icon](class-diagram-toolbar-and-context-menu.html) on the diagram toolbar located on top of the diagram editor.

![Diagram editor](https://resources.jetbrains.com/help/img/idea/2025.3/diagram_editor.png)

The lists are displayed based on the selected visibility level, which you can change. For example, to view protected methods, click ![the Change Visibility Level button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) on the diagram toolbar and select protected from the list. IntelliJ IDEA displays members with visibility not less than protected, such as public, package local, and protected ones. The protected methods are displayed with modifier icons ![key](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.accessProtected.png) next to them.

![Visibility level](https://resources.jetbrains.com/help/img/idea/2025.3/ac_diagrams_visibility_level.png)

You can click the ![the Show Dependencies icon](https://resources.jetbrains.com/help/img/idea/2025.3/uml-support.icons.dependencies.svg) icon to see class dependencies. IntelliJ IDEA follows the [UML conventions](https://en.wikipedia.org/wiki/Class_diagram#Relationships) in showing relationships between the classes.

![class_dependencies.png](https://resources.jetbrains.com/help/img/idea/2025.3/class_dependencies.png)

When you click through classes in the graph, IntelliJ IDEA greys out classes that do not reside in the same package. This might be helpful, when you generate a diagram on a package that contains inner packages.

![different_packages.png](https://resources.jetbrains.com/help/img/idea/2025.3/different_packages.png)

To save the diagram as a file, right-click the diagram editor and from the context menu, select Export Diagram | Export to File and then the file extension in which you want to save the diagram.
