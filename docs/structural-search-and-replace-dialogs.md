[//]: # (Source: https://www.jetbrains.com/help/idea/structural-search-and-replace-dialogs.html)
[//]: # (Downloaded: 2025-12-17 20:03:26)

# Structural search and replace dialogs

Use these dialogs to find and replace fragments of code that structurally match the suggested [search template](search-templates.html).

For more information about the possible usages, refer to the section [Structural search and replace](structural-search-and-replace.html).

Item| Description| Available in  
---|---|---  
Search template| Use this text area to specify the [template](search-templates.html) based on which IntelliJ IDEA performs the search process. You can type the template code in the field or click ![the Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) and select the Existing Templates option to see a list of existing templates.| Both  
Match case| Select this checkbox if you want IntelliJ IDEA to match the case of the code you are searching for.| Both  
File type| Use this option to select a file type for your search. In this case, IntelliJ IDEA searches only in the specified file types.| Both  
![the Filter icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg)| Click this icon to add [modifiers](search-templates.html#ssr_filters) for the whole search template. Use ![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add a new modifier or ![the Remove icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) to remove the existing one.| Both  
![the Settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)| Click this icon to select one of the following options:

  * Save Template: use this option to save a template you have specified in the search template area. IntelliJ IDEA adds the saved template to the User Defined node in the Existing Templates dialog.
  * Export Template to Clipboard: use this option to [export the template](structural-search-and-replace.html#share_template) and share it.
  * Import Template to Clipboard: use this option to [import the shared template](structural-search-and-replace.html#share_template).
  * Existing Templates: use this option to see the list of existing templates. In the Existing Templates dialog, select one of the pre-defined or custom templates. The selected template is displayed in the Preview field. When you click OK, IntelliJ IDEA inserts the source code of the template into the Search template or Replace template field.
  * Switch to Search/Switch to Replace: use this option to quickly switch to the Structural Search or the Structural Replace dialog.

| Both  
Replacement template| Use this text area to specify the [template](search-templates.html) to be substituted. You can type the template code in the field or click ![the Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) and select the Existing Templates option to see a list of existing templates.| Structural Replace  
![Search](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.search.svg)| Click this icon to see the list of your previous searches.| Both  
Shorten fully qualified names| This option makes sense in case the template text contains fully qualified class names. If the checkbox is selected, IntelliJ IDEA automatically reduces these names in the template. Otherwise, fully qualified class names are used.| Structural Replace  
Reformat| Check this option, if you want IntelliJ IDEA to automatically reformat the expanded code fragment according to your code style settings (for more information, refer to the [Code Style](settings-code-style.html) dialog). If the option is not checked, IntelliJ IDEA will only indent the whole template according to the position in code at which it is expanded, leaving its formatting as is.| Structural Replace  
Use static imports| Check this option, if you want IntelliJ IDEA to shorten any references to static elements in the replaced code. IntelliJ IDEA will insert a static import for those elements. The elements are then referenced by their short name. If there are no references to static elements in the replaced code, the option will be ignored.| Structural Replace  
In| Use this area to specify where IntelliJ IDEA should search for and replace your code. You can select from the following options:

  * Project: when you select this option, IntelliJ IDEA searches and replaces the specified template in the whole project.
  * Module: when you select this option, IntelliJ IDEA searches and replaces the specified template in the selected module.
  * Directory: when you select this option, IntelliJ IDEA searches and replaces the specified template in the selected directory.
  * Scope: when you select this option, IntelliJ IDEA searches and replaces the specified template in a certain scope that you have selected. You can select a predefined scope from the available list or create a [custom scope](settings-scopes.html) when you click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg).

| Both  
Search target| Use this option to specify the target of your search process which could be the exact match of the template you have specified (Complete match) or just a part of it. The options of the search target depend on the file type you have selected.| Both  
Open in new tab| If this checkbox is selected, the results of the new search display in a new tab in the Find results tool window. Otherwise, the search results update the existing tab.| Both  
  
28 June 2024

[Work with structural search and replace](tutorial-work-with-structural-search-and-replace.html)[Full-text search in databases](full-text-search-for-databases.html)
