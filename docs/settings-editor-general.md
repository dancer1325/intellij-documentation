[//]: # (Source: https://www.jetbrains.com/help/idea/settings-editor-general.html)
[//]: # (Downloaded: 2025-12-17 20:01:00)

# General

Use the General page of the Settings dialog to configure the editor behaviour and customize its view.

Item| Description  
---|---  
Mouse Control  
Change font size with Ctrl/Command+Mouse Wheel| Enable this option to be able to change font size in the editor by [rolling the mouse wheel](using-code-editor.html#editor_settings) while holding the `Ctrl` key.

  * Select Active editor to change font size only in the current editor tab. If you close and reopen the document, the font size will be reset to the default font or to the color scheme font according to your settings. 
  * Select All editors to change font size in all editor tabs. When you change the font size this way, the new font size is saved in the current color scheme and will apply to all open documents as well as to the newly opened ones. If necessary, you can change it on the Editor | Color Scheme | Color Scheme Font settings page `Ctrl+Alt+S`. 

This checkbox also allows you to change font size in [Quick Documentation popup](viewing-reference-information.html#inline-quick-documentation).  
Move code fragments with drag-and-drop| If this checkbox is selected, you can [drag-and-drop](working-with-source-code.html#editor_lines_code_blocks) code fragments in the editor.  
Soft Wraps  
Soft-wrap these files| Use this field to apply soft wraps to specific file types (For example, it might be helpful when you are writing documentation in markdown files). Enter file extensions separating them with semicolon.You can also enable or disable soft wraps right in the editor:

  * Right-click the left gutter and from the context menu, either select or clear the Soft-Wrap Current Editor option. Keep in mind that these settings affect only the current editor, not a file. ![Soft-Wrap Current Editor](https://resources.jetbrains.com/help/img/idea/2025.3/editor_soft_wraps.png)
  * To quickly access the settings, select Configure Soft Wraps from the list of options.

  
Use the original line's indent for wrapped fragments| Select this checkbox to use custom indentation for soft wraps on resizing the editor or console. Use the Add additional indent field to specify the indent number.  
Only show soft-wrap indicators for the current line| If this checkbox is selected, the soft wrap characters ![Wrap](https://resources.jetbrains.com/help/img/idea/2025.3/soft_wraps.png) ![Wrap](https://resources.jetbrains.com/help/img/idea/2025.3/soft_wrap.png) will be shown in the active logical line only.Otherwise, soft wraps characters will be shown at the end of each line, and at the beginning of each next line.  
Virtual Space  
Allow caret placement| 

  * After the end of line: if this checkbox is selected, you will be able to place the caret anywhere after the last character in any line. As soon as you start typing at a position beyond the end of the line, the necessary number of spaces will be added between the end of the line and the beginning of your input. 
  * Inside tabs: select this checkbox to allow placing the caret inside tab characters. The reason is that each tab character shows in the editor as a set of 'virtual' space characters.

  
Show virtual space at the bottom of the file| If this checkbox is selected, the currently edited line (even if it is the final line) can be scrolled to the top of the screen. IntelliJ IDEA adds the necessary number of virtual lines.  
Scroll Offset| Use this group of options to configure the number of context lines and rows you would like to see around the caret. Also set the minimal number of lines and rows to scroll when the caret gets off the screen.These settings might be helpful if you scroll or navigate in the large file and want to keep track of the caret line. They are also helpful when you use a monitor with vertical orientation.It works similar to [Vim](https://vimhelp.org/options.txt.html) `scrolloff` and `scrolljump` settings.You can configure the following offset options:

  * Vertical scroll offset: offsets number of lines above and below the caret .
  * Vertical scroll jump: offsets number of lines above and below the caret when it jumps off the screen.
  * Horizontal scroll offset: offsets number of rows to the left and to the right of the caret.
  * Horizontal scroll jump: offsets number of rows to the left and to the right of the caret when it jumps off the screen.

  
Caret Movement  
When moving by words| Use this list to configure where the caret should stop when moved by words. You can select from the following options:

  * Jump to current word boundaries: this is the default option. When you move the caret forward (`Ctrl+Right`), IntelliJ IDEA places it to the end of the current word.When you move the caret to the previous word (`Ctrl+Left`), IntelliJ IDEA places the caret at the beginning of the current word.![Jump to current word boundaries](https://resources.jetbrains.com/help/img/idea/2025.3/move_caret_default.png)
  * Always jump to word start: when you select this option, the caret always moves to the beginning of the word.
  * Always jump to word end: when you select this option, the caret always moves to the end of the word. ![Always jump to word end](https://resources.jetbrains.com/help/img/idea/2025.3/always_jump_to_word_end.png)
  * Jump to next/previous word boundaries: when you select this option, the caret moves forward to the start of the next word, and when moved backwards, the caret jumps to the end of the previous word.
  * Stop at both word boundaries: when you select this option, the caret stops at both the start and the end of each word.

  
Upon line break| Use this list to configure where the caret should stop on line breaks. You can select from the following options:

  * Jump to next/previous line boundaries: when you select this option, the caret moves forward to the beginning of the next line, and when moved backwards, the caret jumps to the end of the previous line.
  * Ignore line breaks: when you select this option, IntelliJ IDEA ignores the line breaks, and the caret moves according to the configuration specified in the [Moving by words](#moving_by_word) list.
  * Stop at both line boundaries: when you select this option, the caret stops at both the start and the end of each line.
  * Jump to current line boundaries: when you select this option, the caret always jumps to the end of the current line (when moved forward) or to the beginning of the current line (when moved backwards).Check the following example when you have Always jump to word start specified in the [Moving by words](#moving_by_word) list and Jump to current line boundaries specified in the Upon line break list:![Move caret example](https://resources.jetbrains.com/help/img/idea/2025.3/move_caret_line_break_example.png)
  * Always jump to line start: when you select this option, the caret always moves to the start of a line.
  * Always jump to line end: when you select this option, the caret always moves to the end of a line.

  
Scrolling  
Enable smooth scrolling| If this option is enabled, the editor scrolls the page when you navigate to an element, instead of just jumping to the target location.  
Caret behavior| 

  * Keep the caret in place, scroll editor canvas: select this option to choose scrolling editor canvas and keeping the caret at place.This can be helpful in course of [debugging session](debugging-code.html). As you step through the lines of code, the editor canvas scrolls, while the line at caret is always in the center of the screen.
  * Move caret, minimize editor scrolling: click this option to choose moving the caret.When you step through the lines of code during the [debugging session](debugging-code.html), the caret moves down, and the editor canvas doesn't scroll until the caret line reaches the bottom of the screen.

  
Rich-Text Copy  
Copy (`Ctrl+C`) as rich text| Select this checkbox to copy a rich text from the editor to any other editor that recognizes RTF. Otherwise, the IDE copies a plain text.You can override the unselected option using the Copy as Plain Text or the Copy as Rich Text option from the context menu in your editor.  
Color scheme for copied fragment| Use this list to select a color scheme for the text copy. You can select from the following options: 

  * Active scheme
  * Light
  * Dark
  * High Contrast
  * Classic Light
  * Darcula
  * Darcula Contrast

  
On Save  
Remove trailing spaces on| Select the mode in which IntelliJ IDEA will handle trailing spaces at the end of lines on file saving:

  * Modified lines: strips trailing spaces only at the end of modified lines.
  * All lines: strips trailing spaces in all lines.

  
Keep trailing spaces on caret line| If this option is unselected, trailing spaces will be stripped on the line where the caret is placed on save operation.  
Remove trailing blank lines at the end of saved files| If this checkbox is unselected, IntelliJ IDEA will keep the trailing blank lines on saving files.  
Ensure every saved file ends with a line break| Select this checkbox to have IntelliJ IDEA automatically add an empty line at the end of a file during the save procedure.  
  
Significant trailing spaces that affect the output of a program are not removed where applicable. For example, trailing spaces in multiline strings in Groovy are not removed and so on.

12 November 2024

[Editor](settings-editor.html)[Auto Import](settings-auto-import.html)
