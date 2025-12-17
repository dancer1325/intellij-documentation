[//]: # (Source: https://www.jetbrains.com/help/idea/terminal-emulator.html)
[//]: # (Downloaded: 2025-12-17 20:04:08)

## Terminal engine

Currently, the following terminal engines are available in IntelliJ IDEA:

  * Reworked 2025 (default). Starting from version 2025.2, this is the default terminal engine in IntelliJ IDEA. It is designed to combine the stability of the Classic emulator with improved performance, compatibility, and modern enhancements.

  * Classic. This is a standard terminal emulator of the previous generation, built on the [JediTerm](https://github.com/JetBrains/jediterm) library, with user input (commands and keystrokes) sent directly to the underlying shell.




The Experimental 2024 (deprecated) terminal engine, also known as New Terminal in IntelliJ IDEA 2024.*, has been deprecated due to compatibility challenges. The option to select this terminal engine is available only to users who had enabled it in IntelliJ IDEA 2024.*. You can find the documentation for it in the [earlier version of IntelliJ IDEA Help](https://www.jetbrains.com/help/idea/2024.3/terminal-emulator.html#new-terminal).

Learn more about the terminal engines [from our blog post](https://blog.jetbrains.com/idea/2025/04/jetbrains-terminal-a-new-architecture).

### Select a Terminal engine

  1. Open the Terminal tool window: View | Tool Windows | Terminal.

  2. In the tool window header, click ![Options](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) and select a terminal engine.

![Terminal Select Engine](https://resources.jetbrains.com/help/img/idea/2025.3/terminal_select_engine.png)

Alternatively, open the IDE settings (`Ctrl+Alt+S`) and go to Tools | Terminal | Terminal engine.



