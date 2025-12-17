[//]: # (Source: https://www.jetbrains.com/help/idea/settings-editor-appearance.html)
[//]: # (Downloaded: 2025-12-17 20:00:56)

# Appearance

Use this page to customize the editor appearance.

Item| Description  
---|---  
Caret blinking (ms)| Select this checkbox to make the caret blink with the specified period (in milliseconds).  
Use block caret| Select this checkbox to have the block caret applied in the Insert mode and the usual caret applied in the Overwrite mode. Clear this checkbox to have the usual caret applied in the Insert mode and the block caret applied in the Overwrite mode.  
Use full line height caret| Select this checkbox to have the caret height the same as the height of the line.  
Highlight occurrences of selected text| Highlight all occurrences of the selected text within a file. This helps track where the selected text appears throughout your code and manage repetitive fragments.  
Show hard wrap and visual guides (configured in Code Style options)| Select this checkbox to have a thin vertical line at the right margin of the editor displayed. Refer to the description of the [Code Style settings](settings-code-style.html).  
Show line numbers| Select this checkbox to have line numbering shown in the editor gutter. You can select the [Absolute, Relative, or Hybrid](editor-gutter.html#line-numbers) option from the list.  
Show method separators| Select this checkbox to have thin lines displayed in classes to separate methods from each other and to separate methods from field declarations.   
Show whitespaces| Select this checkbox to have IntelliJ IDEA display whitespaces or tabs (depending on the [Code Style settings](settings-code-style.html)).You can select the following options:

  * Leading: add whitespaces before your code line.
  * Inner: display whitespaces inside the line of your code.
  * Trailing: display whitespaces after the code line.
  * Selection: display whitespaces in code fragments that you have selected in the editor.

  
Show indent guides| Select this checkbox to display vertical lines in the editor to indicate positions of indents and thus facilitate typing, manual formatting, reading, and maintaining code.  
Show intention bulb| Whenever IntelliJ IDEA detects that your code can be modified or improved, [a light bulb icon](intention-actions.html) appears on the current line in the editor: ![the Intention action icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.codeInsight.intentionBulb.svg) for intention actions and ![the Quick-fix icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.codeInsight.quickfixBulb.svg) for quick-fixes. Clear this checkbox if you don't want to see these icons. You can still access the list of available actions and quick-fixes by pressing `Alt+Enter`.  
Show preview for intention actions when available| Automatically open the preview for [intention actions](intention-actions.html).When the option is disabled, you can press `Ctrl+Q` in the list of available intentions to toggle the preview on.  
Render documentation comments| Select this checkbox to always render documentation comments as text paragraphs with proper formatting and links right in the editor. [Rendered comments](javadocs.html#toggle-rendered-view) are easier to read, and they don't overload your code with extra tags.  
Show code lens on scrollbar hover|  Select this checkbox to enable the [lens mode](using-code-editor.html#lens_mode_code).   
Use editor font for inlay hints| Select this checkbox to use the font of the editor text instead of the inlay hints font, which is defined in the [color scheme](configuring-colors-and-fonts.html).  
Enable HTML/XML tag tree highlighting| Select this checkbox to show the hierarchy of tags highlighted with different colors. If this option is enabled, you can define the following options:

  * Levels to highlight: specify the depth of hierarchy to be highlighted.
  * Opacity: specify brightness of highlighting

![Tags highlighting](https://resources.jetbrains.com/help/img/idea/2025.3/tags_highlighting.png)Highlighting is activated when there is more than one tag with the same name in the hierarchy.  
Show CSS color preview as background| If this checkbox is selected, the background of the color value shows the color preview:![Showing CSS color preview in the background](https://resources.jetbrains.com/help/img/idea/2025.3/color_preview_background.png)By default, IntelliJ IDEA also shows color preview icons in the gutter. Clicking such icon invokes the Color Picker where you can change the color value.![Click color gutter icon to open the color picker](https://resources.jetbrains.com/help/img/idea/2025.3/colorPreview_color_picker.png)To hide these gutter icons, clear the Color preview checkbox on the Editor | General | Gutter Icons settings page `Ctrl+Alt+S`.For more information, refer to [Managing colors](style-sheets.html#ws_css_change_color_values).  
Highlight RDoc and ruby in comments|  This feature is only supported when Ruby plugin is installed!If this checkbox is selected, the keywords are highlighted in comments. Otherwise, they are displayed as plain text.Changing state of this checkbox takes effect upon IntelliJ IDEA restart only.  
Show closing labels in Dart source code| This feature is only supported when the Dart plugin is installed!By default, IntelliJ IDEA inserts autogenerated comments (closing labels) after the closing parentheses of objects within the `build()` method in Dart code. Clear the checkbox to suppress adding closing labels.  
  
20 May 2025

[Auto Import](settings-auto-import.html)[Breadcrumbs](settings-editor-breadcrumbs.html)
