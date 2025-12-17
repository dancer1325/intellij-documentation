[//]: # (Source: https://www.jetbrains.com/help/idea/touch-bar-support.html)
[//]: # (Downloaded: 2025-12-17 20:04:30)

# Touch bar support

The Touch Bar is located above the keyboard on supported Apple MacBook Pro models. It provides additional controls for quick access based on the current context.

Starting from version 2025.1, touch bar support has been disabled by default in IntelliJ IDEs.

### Enable the Touch Bar support

  1. Press `Ctrl+Shift+A` or choose Help | Find Action from the main menu. In the popup that opens, start typing `Registry`, select the corresponding item and press `Enter`. 

  2. Start typing `ide.mac.touchbar.enabled`.

  3. Enable the `ide.mac.touchbar.enabled` option by selecting the checkbox under Value. 

![Registry window](https://resources.jetbrains.com/help/img/idea/2025.3/registry_touchbar.png)
  4. Restart the IDE.


![The Touch Bar](https://resources.jetbrains.com/help/img/idea/2025.3/TouchBarMainContext.png)

The Control Strip in the right part of the Touch Bar includes controls for system-level tasks that are usually accessed with function keys on classic keyboards. The app region to the left of the Control Strip contains controls that are specific to IntelliJ IDEA and the current context. One more system button is located in the left part of the Touch Bar; this is usually the Escape key, but it can be something else depending on the context.

IntelliJ IDEA provides the following contexts:

  * Default context is used most of the time.

It includes controls for running, building, and debugging the application with the ability to quickly select or create a new [run/debug configuration](run-debug-configuration.html). It also provides VCS controls for updating your project and committing changes, which can be replaced in some contexts (for example, with the refresh action when the focus is on the [Maven tool window](maven-projects-tool-window.html) or the [Gradle tool window](jetgradle-tool-window.html)) .

![Default context with Maven refresh](https://resources.jetbrains.com/help/img/idea/2025.3/TouchBarMainContextMaven.png)

For more controls, you can use modifier keys: `Ctrl`, `Alt`, `Shift`, and `⌥+⌘`.

  * Debugger context is used when the focus is on the [Debug window](debug-tool-window.html).

It includes controls to stop, pause, resume the debugger, as well as stepping and evaluating expressions.

![The Touch Bar in debugger context](https://resources.jetbrains.com/help/img/idea/2025.3/TouchBarDebuggerContext.png)

For more controls, hold down the `Alt` key.

  * When the focus is on a dialog, confirmation controls are displayed (for example, Cancel, Apply, OK, or other relevant buttons).

![The Touch Bar with dialog confirmation buttons](https://resources.jetbrains.com/help/img/idea/2025.3/TouchBarDialog.png)

  * When you start typing inside a popup with a list of actions, the actions are filtered according to what you type (for example, in the Project tool window `Alt+1`, when you press `Alt+Insert`, you can filter the types of files you would like to create). When the popup is active, the touch bar contains the same list of items, and it is filtered accordingly as you type.

![The Touch Bar with filtered popup items](https://resources.jetbrains.com/help/img/idea/2025.3/TouchBarPopup.png)




### Customize the Touch Bar

You can configure the controls displayed on the Touch Bar in the default and debugger context.

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Appearance & Behavior | Menus and Toolbars.

  2. Expand the Touch Bar node and configure the controls for corresponding contexts and modifier keys.

The Touch Bar node is available only if you are using an Apple MacBook Pro with the Touch Bar.

  3. Apply changes when finished.




To show the function keys (`F1`, `F2`, and so on) on the Touch Bar, hold down the `Fn` key. You can also make function keys display permanently for selected applications, as described in the following [Apple support article](https://support.apple.com/en-us/HT207240).

IntelliJ IDEA provides an option to always show function keys without the need to change system settings:

### Show function keys

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Keymap.

  2. Select Show F1, F2, etc. keys on the Touch Bar at the bottom.




22 October 2025

[Presentation Assistant](presentation-assistant.html)[Colors and fonts](configuring-colors-and-fonts.html)
