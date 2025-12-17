[//]: # (Source: https://www.jetbrains.com/help/idea/multicursor.html)
[//]: # (Downloaded: 2025-12-17 19:32:53)

## Add and remove carets

There are two options of where on the code line the carets can be added:

To existing characters| Using virtual spaces  
---|---  
If there is no character, tab, or whitespace at the position where you want to add a new caret, the new caret will be added to the last character position in the target line.| This way you can add new carets anywhere after the last character in any line. As soon as you start typing at a position beyond the end of the line, the necessary number of spaces will be added between the end of the line and the beginning of your input. You can enable virtual spaces by selecting the Allow placement of caret after end of line checkbox on the Editor | General settings page `Ctrl+Alt+S`. Alternatively, virtual spaces are also enabled in the [column selection mode](#column_selection).  
  
### Add or remove carets at selected locations using mouse

  * `Alt+Shift+Click` at the target location to add another caret.

![Add multiple carets using mouse](https://resources.jetbrains.com/help/img/idea/2025.3/multi_carets.png)
  * `Alt+Shift+Click` at one of the multiple carets to remove it. The last caret will not be removed.




### Add carets above or below the current caret using keyboard

  * Press `Ctrl` twice, and then without releasing it, press up or down arrow keys.

If [virtual spaces](#column_selection) are enabled, new carets will be added exactly above or below the current caret position. Otherwise, in lines, which are shorter than the current offset, carets will be added at line ends.

![Add multiple carets using keyboard](https://resources.jetbrains.com/help/img/idea/2025.3/add_carets_with_ctrl.png)
  * Enable the [column selection mode](#column_selection) (press `Alt+Shift+Insert`) and then press `Shift+Up`/`Shift+Down`.

  * Press `Ctrl+Shift+A`, type Clone caret, and choose the desired action from the suggestion list.

![Clone caret](https://resources.jetbrains.com/help/img/idea/2025.3/go_multicursor1.png)

By default, these actions are not associated with keyboard shortcuts. You can assign your custom shortcuts to these actions as described in [configuring keyboard shortcuts](configuring-keyboard-and-mouse-shortcuts.html).




### Add carets at each line of the current document

  * Press `Ctrl+Home` to place the caret at the beginning of the first line, enable the [column selection mode](#column_selection) (press `Alt+Shift+Insert`), and then press `Ctrl+Shift+End`.




### Add carets to the end of each line in the selected block

  * Select a code block in the editor and then press `Alt+Shift+G` or go to Edit | Add Carets to Ends of Selected Lines in the main menu.




### Remove multiple carets

  * Press `Esc` to delete all existing carets, except the one that was added last.

  * `Alt+Shift+Click` at one of the multiple carets to remove it. The last caret will not be removed.



