[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-code-style.html)
[//]: # (Downloaded: 2025-12-17 19:21:43)

## Configure schemes

In IntelliJ IDEA, code style settings are language-specific, so you need to configure them for every language that you use in your project separately. You can also copy the settings from one language and apply them to another language.

### Configure a code style scheme

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style.

To configure a scheme [for new projects](configure-project-settings.html#new-default-settings), go to File | New Projects Setup | Settings for New Projects | Editor | Code Style.

  2. Select the language for which you want to configure the code style. 

  3. Select the code style Scheme that you want to configure: the [Project](#project-scheme) scheme or one of the [IDE-level schemes](#default-scheme).

Click ![Show Scheme Actions](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) next to the Default scheme and select Duplicate to create a copy of the scheme.

  4. Browse through the tabs and configure code style preferences.

For a detailed description of each setting for Java, refer to [Code Style. Java](code-style-java.html).

Use the right section of the dialog to preview the changes. When you change a setting, one or several blinking areas appear in the preview area emphasizing the changes.




### Apply a predefined code style

In some languages, for example, in PHP, there are predefined coding standards that you can upload to the IDE and apply to your code.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style.

To configure a scheme [for new projects](configure-project-settings.html#new-default-settings), go to File | New Projects Setup | Settings for New Projects | Editor | Code Style.

  2. Select the language for which you want to configure the code style.

  3. Select the code style Scheme that you want to modify: the [Project](#project-scheme) scheme or one of the [IDE-level schemes](#default-scheme).

  4. Click the Set from link, select Predefined, and select one of the pre-configured standard from the list.




### Apply code style from another language

For most of the supported languages, you can copy code style settings from other languages or frameworks.

Copying styles between languages is not supported for C#, Visual Basic, and other .NET-specific languages.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style.

To configure a scheme [for new projects](configure-project-settings.html#new-default-settings), go to File | New Projects Setup | Settings for New Projects | Editor | Code Style in the main menu.

  2. Select the language for which you want to configure the code style.

  3. Select the code style Scheme that you want to modify: the [Project](#project-scheme) scheme or one of the [IDE-level schemes](#default-scheme).

  4. Click Set from in the upper-right corner.

The link is shown only if it is possible to apply code style settings from another language.

  5. From the list that appears, select the language to copy the code style from.

Only applicable settings are copied from another language, other settings are left intact.

![Set code style from another language](https://resources.jetbrains.com/help/img/idea/2025.3/set-codestyle-from-language.png)


