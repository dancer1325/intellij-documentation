[//]: # (Source: https://www.jetbrains.com/help/idea/troubleshoot-common-scala-issues.html)
[//]: # (Downloaded: 2025-12-17 20:04:35)

## Why is my code highlighted incorrectly?

The Scala plugin uses its own type checker and performs its own type inference in real time, while you type your code. The type checking is optimized for editing rather than compiling code. Its logic is independent of the Scala compiler so that it can work with incomplete code and doesn't require prior compilation. However, it also means that sometimes the results of the Scala plugin type checking differ from the Scala compiler – and that's a bug.

Typically this happens when the code is complex, and you just made an important modification. The type checker might need time to catch up, and occasionally it might fail.

  * Try to update IntelliJ IDEA and the Scala plugin. It is possible that you experience an issue that was already reported and fixed.

  * You may also look through our list of open and fixed tickets on [our YouTrack](https://youtrack.jetbrains.com/issues/SCL). If you find a ticket describing an issue similar to yours, and it's fixed, but not yet released on the Public update channel, you may consider [switching to the Nightly update channel](get-started-with-scala.html#ChannelUpdate).

  * If the above doesn't work then, first, create a ticket for us.

  * If the type-aware highlighting highlights the correct code, and it's an error that rarely happens, try to disable the highlighting locally.

    1. Highlight the code and from the main menu select Code | Surround With.

    2. Select the / * _ * /.../ * _ * / option from the list.

![Surround code action](https://resources.jetbrains.com/help/img/idea/2025.3/T_surround_with_action.png)

The error is not highlighted anymore.

![Surround code action - result](https://resources.jetbrains.com/help/img/idea/2025.3/T_surround_with_action_result.png)

The type-aware highlighting ![Type-aware highlighting icon](https://resources.jetbrains.com/help/img/idea/2025.3/type_aware_highlighting_icon.png) is enabled in your project by default. To disable it, find its icon in the bottom-right corner of the window and click on it. Click again to enable the highlighting.

  * If a lot of code is highlighted incorrectly, consider enabling Compiler-based highlighting. Go to Settings | Languages & Frameworks | Scala and on the Editor tab, change the error highlighting to Compiler.

![Scala compiler-based highlighting](https://resources.jetbrains.com/help/img/idea/2025.3/scala_compiler_based_highlighting.png)

However, before that, think about possible drawbacks. Compiler-based highlighting is slower, it requires more resources (type checking is done twice, .class files are generated), the highlighted code does not come with quick-fixes proposals, it is not optimized for on-the-fly editing, and requires full compilation of the project, which means it might not work for incomplete code.



