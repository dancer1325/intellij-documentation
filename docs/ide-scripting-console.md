[//]: # (Source: https://www.jetbrains.com/help/idea/ide-scripting-console.html)
[//]: # (Downloaded: 2025-12-17 19:29:10)

# IDE scripting console

The IDE Scripting Console can be used to write simple scripts that automate IntelliJ IDEA features and extract various information. With access to the [IntelliJ Platform API](https://plugins.jetbrains.com/docs/intellij/welcome.html), you can think of it as a lightweight alternative to a plugin, which adds or modifies some behavior of the IDE.

By default, it supports scripts written in Kotlin, JavaScript, and Groovy. However, you can use any scripting language that is compliant with [JSR 223](https://www.jcp.org/en/jsr/detail?id=223), for example, Python, Ruby, Clojure, and so on.

Some information and examples are available in [this gist](https://gist.github.com/gregsh/b7ef2e4ebbc4c4c11ee9).

### Open the IDE Scripting Console

  1. Press `Ctrl+Shift+A` and type `IDE Scripting Console`. Once the required option is located, click it to run the console.

  2. This opens the IDE Scripting Console tab in the editor, where you can type code and execute it using `Ctrl+Enter`.

For example, create a Kotlin script with the following code:

import com.intellij.openapi.ui.Messages.showInfoMessage var sum: Long = 0L val arr = "35907 77134 453661 175096 23673 29350".split(" ") arr.forEach { sum+=it.length } showInfoMessage((sum.toFloat() / arr.size).toString(), "test") 

Select it all with the mouse pointer or `Ctrl+A` and then press `Ctrl+Enter` to run it. You should see the result of executing each line in the Run tool window and a popup dialog titled test with the average length of numbered elements in the array. Click OK to close it.

If nothing is selected, only the current line with the caret is executed.




The scripts are stored in the [Configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory) under consoles/ide. You can also see them in the Project tool window under Scratches and Consoles/IDE Consoles. If you add a file named .profile followed by the designation of the corresponding language to this directory (for example, .profile.groovy), it will be executed along with any script that you run. Use the profile to define functions for your scripts.

22 November 2024

[JShell Console](jshell-console.html)[File Watchers](using-file-watchers.html)
