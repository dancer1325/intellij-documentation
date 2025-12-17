[//]: # (Source: https://www.jetbrains.com/help/idea/full-line-code-completion.html)
[//]: # (Downloaded: 2025-12-17 19:27:18)

# Full Line code completion

The Full Line code completion feature uses a locally run deep learning model to suggest entire lines of code. It is available in IntelliJ IDEA with the Ultimate subscription out of the box and does not require an additional license. 

Full Line code completion runs entirely on your local device without sending any code over the internet.

Suggestions are displayed in the editor as you type Java, Kotlin, JavaScript/TypeScript, or CSS code.

  * To accept an entire suggestion, press `Tab`.

Alternatively, go to Code | Code Completion | Insert Inline Proposal in the main menu or [configure a different shortcut](#change-completion-shortcut).

  * To accept a suggestion word by word, press `Ctrl+Right` or go to Code | Code Completion | Insert Inline Proposal's Word in the main menu.

  * To accept a suggestion line by line, press `End` or go to Code | Code Completion | Insert Inline Proposal's Line in the main menu.




The IDE formats all suggestions and adds required brackets and quotes.

Each supported language has its own set of suggested code checks. The most basic ones, like unresolved reference checks, are available for most of the languages to guarantee that the IDE does not suggest non-existent variables and methods.

Full Line completion supports auto-import and uses smart filtering to avoid showing suggestions that tend to be canceled explicitly or deleted right after they were accepted.

In IntelliJ IDEA, Full Line completion is available also for Python, TypeScript, PHP, Go, and Ruby. To be able to use the feature with these languages, install a corresponding language plugin as described in [Install a plugin from Marketplace](managing-plugins.html#install_plugin_from_repo).

### Check system requirements

  * Full Line code completion requires a computer with an x64 processor that supports [AVX2](https://en.wikipedia.org/wiki/Advanced_Vector_Extensions), or an ARM64 processor. If the AVX2 support is missing, Full Line Code Completion will be automatically disabled.




### Enable the Full Line Code Completion plugin

This functionality relies on the [Full Line Code Completion](https://plugins.jetbrains.com/plugin/14823-full-line-code-completion) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Full Line Code Completion plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Full Line Code Completion plugin, and select the checkbox next to the plugin name.




### Enable and configure Full Line completion

  1. Press `Ctrl+Alt+S` to open settings and select Editor | General | Inline Completion.

  2. Select the Enable local Full Line completion suggestions checkbox and select the languages that you want to use Full Line completion with.

Models for Java and Kotlin are bundled with IntelliJ IDEA.

For some languages, for example, for CSS and JavaScript / TypeScript, you need to manually download models by clicking Download to enable completion.

![Enabling full line code completion](https://resources.jetbrains.com/help/img/idea/2025.3/ij_full_line_completion_enable.png)
  3. Configure completion options:

     * Use the Enable automatic completion on typing option to display completion suggestions only when you press `Alt+Shift+\`, rather than automatically as you type.

     * Use the Enable multi-line suggestions option to get multi-line completion suggestions together with single-line suggestions.

     * Enable Synchronize inline and popup completions to view Full Line completion suggestions alongside regular completion. In this case, Full Line suggestions are marked with ![](https://resources.jetbrains.com/help/img/idea/2025.3/ml-inline-completion.icons.full-line.svg) in the list of suggestions.

![Full Line completion suggestions in completion list](https://resources.jetbrains.com/help/img/idea/2025.3/ij_flcc_icon_in_suggestions.png)



Full Line completion runs locally using the models that are downloaded to your computer. From the Download models list, select the way to update these models. You can update the models automatically, manually, or confirm every update in a notification.

### Change the completion shortcut

You can change the default inline completion shortcut that you use to accept suggestions.

  1. Hover over the suggestion.

  2. In the popup that appears, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.chevronDownLarge.svg) and select the key that you want to use for accepting suggestions, for example, `Right`.

To assign your own shortcut, select Custom.

![Full line code completion popup](https://resources.jetbrains.com/help/img/idea/2025.3/ij_full_line_completion_popup.png)
  3. For quick access to the Full Line completion settings, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) in the popup.




You can also use [inline code completion in AI Assistant](https://www.jetbrains.com/help/ai-assistant/code-completion.html), which automatically completes entire functions and blocks of code based on the context of your project.

16 July 2025

[Code completion](auto-completing-code.html)[Advanced completion](advanced-code-completion.html)
