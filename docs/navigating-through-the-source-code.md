[//]: # (Source: https://www.jetbrains.com/help/idea/navigating-through-the-source-code.html)
[//]: # (Downloaded: 2025-12-17 19:32:55)

## Navigate between code elements

### Go to declaration and its type

You can navigate to the initial declaration of a symbol and the symbol's type from its usage.

  * Place the caret at the necessary symbol and press `Ctrl+B`. 

![Go to Declaration](https://resources.jetbrains.com/help/img/idea/2025.3/goto_declaration_from_usages.png)
  * For a type declaration, press `Ctrl+Shift+B`.




### Go to implementation

You can keep track of class implementations and overriding methods using the gutter icons in the editor, or by pressing the appropriate shortcuts, or by clicking Inheritors inlay hints.

  * Click one of the ![the Implemented method icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.implementedMethod.svg)/![the Implementing method icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.implementingMethod.svg), ![the Overridden method icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.gutter.overridenMethod.svg)/![the Overriding method icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.gutter.overridingMethod.svg) gutter icons located in the editor and select an ascendant or descendant class from the list. 

![Gutter icons](https://resources.jetbrains.com/help/img/idea/2025.3/implementations.png)
  * To navigate to the super method, press `Ctrl+U`.

  * To navigate to the implementation, press `Ctrl+Alt+B`.

  * Use Inheritors hints that are displayed next to a class or an interface and show the number of its descendants. Click the hint to jump to the descendant. If there are several implementations, select the relevant one from the list.

Inheritors inlay hints are enabled by default. To turn them off, hover over a hint and select Hide 'Code Vision: Inheritors' Inlay Hints or Hide All 'Code Vision' Inlay Hints from the context menu. 

![Hide Inheritors hints in the editor](https://resources.jetbrains.com/help/img/idea/2025.3/ws_code_vision_inheritor_hide.png)

By default, Inheritorshints are shown above classes and interfaces. To change this position, click Configure from the context menu of a hint. 

![Inheritors hints: configure position](https://resources.jetbrains.com/help/img/idea/2025.3/ws_code_vision_configure.png)

On the Inlay Hints page, that opens, select the appropriate setting from the Position list. Alternatively, select the Code vision node and change the Default position for metrics. 

![Code vision: configure position in the Settings dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ws_code_vision_default_settings.png)



### Navigate between errors or warnings

  * To jump to the next or previous found issue in your code, press `F2` or `Shift+F2` respectively. Alternatively, go to Navigate | Next / Previous Highlighted Error in the main menu.

IntelliJ IDEA places the caret immediately before the code issue.

  * Configure the way IntelliJ IDEA navigates between code issues: it can either jump between all code issues or skip minor issues and only navigate between detected errors. Right-click the code analysis marker in the scroll bar area and choose one of the available navigation modes from the context menu:

    * To have IntelliJ IDEA skip warnings, infos, and other minor issues, choose Problems with Highest Priority.

    * To have IntelliJ IDEA jump between all detected code issues, choose All Problems.




### Show siblings

You can view the implementations of methods in the neighboring classes in a separate popup.

  1. In the editor, place the caret at the method's name.

  2. In the main menu, go to View | Show Siblings. 

IntelliJ IDEA opens a popup where you can browse through the implementations, navigate to source, edit code, and open the list in the Find tool window.

![Show siblings](https://resources.jetbrains.com/help/img/idea/2025.3/show_siblings.png)



### Browse through methods

  * Press `Alt+Down` or `Alt+Up`.

  * To visually separate methods in code, in the Settings dialog (`Ctrl+Alt+S`) , go to Editor | General | Appearance and select the Show method separators option.

![Method Separators in Editor](https://resources.jetbrains.com/help/img/idea/2025.3/methods_separators.png)
  * To open the Structure tool window, press `Alt+7`.



