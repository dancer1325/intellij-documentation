[//]: # (Source: https://www.jetbrains.com/help/idea/scala-decompile-see-bytecode.html)
[//]: # (Downloaded: 2025-12-17 19:59:45)

# Decompile and see the bytecode of Scala code

IntelliJ IDEA allows you to decompile the bytecode produced by the Scala compiler to Java and to examine the bytecode directly.

### Install the required plugins

This functionality relies on the Java Bytecode Decompiler and and Bytecode Viewer plugins, which are bundled and enabled in IntelliJ IDEA by default.

If the relevant features are not available, make sure that you did not disable the plugins.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Java Bytecode Decompiler and Bytecode Viewer plugins, and click Enable. Restart the IDE if prompted.




### Show decompiled class as Java

  1. Build your project by clicking Build | Build Project in the main menu or by pressing `Ctrl+F9`. Alternatively, run the project by pressing `Shift+F10`.

  2. In the Project tool window (`Alt+1`), open the target folder, right-click the `.class` file you want to decompile, and select Show Decompiled Class As Java.

  3. The decompiled code will show up in the editor.


![Show Decompiled Class As Java](https://resources.jetbrains.com/help/img/idea/2025.3/scala_decompileasjava.png)

Learn more from the [Java Bytecode Decompiler](decompiler.html) page.

### Show bytecode

  1. Build your project by clicking Build | Build Project in the main menu or by pressing `Ctrl+F9`. Alternatively, run the project by pressing `Shift+F10`.

  2. In the Project tool window (`Alt+1`), select a class, case class, object, case object, or an enum file.

  3. In the main menu, go to View | Show Bytecode. IntelliJ IDEA will display a dialog with the bytecode.


![Show Bytecode](https://resources.jetbrains.com/help/img/idea/2025.3/scala_bytecode_viewer.png)

There are limitations to what the decompiler can do:

  * The bytecode you want to see should exist: the project should be compiled successfully, and the file you selected should be in use, as the compiler sometimes ignores dead code during compilation.

  * The file you selected should contain one and only one class, case class, and so on.

  * The decompiler will not display the bytecode for the Scala file with top-level definitions.




Learn more from [Show bytecode for compiled files](decompiler.html#show-bytecode).

16 January 2025

[Troubleshoot common Scala issues](troubleshoot-common-scala-issues.html)[sbt](sbt-support.html)
