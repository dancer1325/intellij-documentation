[//]: # (Source: https://www.jetbrains.com/help/idea/internationalization-and-localization.html)
[//]: # (Downloaded: 2025-12-17 19:30:00)

# Internationalization and localization

Internationalization (i18n) refers to the process of extracting strings from source code and presenting them as properties with a set of values.

Localization (l10n) is the process of translating values of these properties into target languages.

Keys and values for the target languages are stored in dedicated [properties files](properties-files.html), which can be combined into a [resource bundle](resource-bundle.html) for convenience. IntelliJ IDEA can recognize [hard-coded string literals](hard-coded-string-literals.html) in Java code and suggest extracting them into the corresponding properties files.

### Install the Resource Bundle Editor plugin

Install the Resource Bundle Editor plugin to be able to work with properties:

  1. In the Settings dialog `Ctrl+Alt+S`, select Plugins.

  2. Switch to the Marketplace tab and type `Resource Bundle Editor` in the search bar.

  3. Click Install next to the plugin name. Apply the changes and close the dialog. 




16 October 2024

[Macros](using-macros-in-the-editor.html)[Properties files](properties-files.html)
