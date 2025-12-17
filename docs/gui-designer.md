[//]: # (Source: https://www.jetbrains.com/help/idea/gui-designer.html)
[//]: # (Downloaded: 2025-12-17 19:28:30)

# GUI Designer

Item| Description  
---|---  
Generate GUI into| This option specifies what kind of output the GUI Designer generates for the visual forms you create.If your build actions are [delegated to Gradle](work-with-gradle-projects.html#delegate_build_actions), GUI Designer will not generate Java source code.The available settings are:

  * Binary class files. This is the default option. When selected, no Java source code is generated for GUI forms and components. When the project compiles, IntelliJ IDEA creates the necessary compiled runtime classes.
  * Java source files .If this option is selected, the GUI Designer writes Java source code for the form and its components to the source file of the class to which the form is bound, on compiling, running or debugging. During compilation, two blocks of code are added to the form's class:
    * A private method `$$$setupUI$$$()` that contains the GUI initializer code for the bound form and its components.
    * A call to the `$$$setupUI$$$()` method.
Do not change the generated method, or call it from any other code. If you manually modify GUI initializer code, your UI will no longer be in sync with the .form file, and the next compilation will overwrite your changes.

  
Automatically copy form runtime classes to the output directory| If this option is checked, the classes from the package `com.intellij.uiDesigner.core` package are copied to the configured output directory, when the project is compiled. These classes are used when working with the GridLayoutManager(IntelliJ), or when there are components with mnemonics, specified by the `&` character.  
Default Layout Manager| Set the default layout manager for new components placed into forms. The selection here appears as the setting for the Layout Manager property whenever a new component is placed on a form.

  * BorderLayout: Design-time behavior in forms emulates Java's Border layout manager.
  * CardLayout: Design-time behavior in forms emulates Java's Card layout manager.
  * FlowLayout: Design-time behavior in forms emulates Java's Flow layout manager.
  * FormLayout (JGoodies): Design-time behavior in forms emulates JGoodies Forms layout manager. (For more information, refer to <https://jgoodies.dev.java.net/>)
  * GridBagLayout: Design-time behavior in forms emulates Java's Grid Bag layout manager.
  * GridLayoutManager (IntelliJ): Design-time behavior in forms is controlled by this custom layout manager. It's basically a simple grid layout scheme that's sufficient for many uses. It is the default layout manager in new IntelliJ IDEA installations.

  
Default accessibility for UI-bound fields| Use this option, if you want to change the default accessibility for UI-bound fields from `private` to something else, like `public`.  
Resize column and row headers with mouse| This checkbox enables/disables resizing in captions. If this checkbox is selected, IntelliJ IDEA allows you to resize column and rows using mouse. When pointing to a column or a row, the mouse pointer changes its shape to the double arrow.  
  
21 June 2024

[Emmet](settings-emmet.html)[Language Injections](language-injections-settings.html)
