[//]: # (Source: https://www.jetbrains.com/help/idea/using-macros-in-the-editor.html)
[//]: # (Downloaded: 2025-12-17 20:05:31)

## Example: Combine reformatting and saving into one action

This example shows how to create a macro that [reformats the current file](reformat-and-rearrange-code.html) `Ctrl+Alt+L` and saves your project when you press `Ctrl+S`.

  1. [Record a macro](#record-a-macro-reformat-save) with the reformat and save actions.

  2. [Bind](#bind-macro) the `Ctrl+S` shortcut to the created macro.




### Record the macro

  1. Open any file in the editor.

  2. In the main menu, go to Edit | Macros | Start Macro Recording.

  3. Press `Ctrl+Alt+L` to reformat code (Code | Reformat Code) and then press `Ctrl+S` to save all changes (File | Save All). IntelliJ IDEA will show the performed actions in the status bar. 

![Macro recording](https://resources.jetbrains.com/help/img/idea/2025.3/rm_macros_recording.png)
  4. Select Edit | Macros | Stop Macro Recording.

  5. In the Enter Macro Name dialog, specify the name for the new macro and click OK.

![Enter Macro Name dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ij_reformat_and_save_macro.png)



### Assign a shortcut for the new macro

  1. Press `Ctrl+Alt+S` to open settings and then select Keymap. 

  2. Expand the Macros node and select the created Reformat and Save macro.

  3. Right-click the macro and choose Add Keyboard Shortcut in the context menu.

![Add Keyboard Shortcut](https://resources.jetbrains.com/help/img/idea/2025.3/ij_macro_add_keyboard_shortcut.png)
  4. In the Keyboard Shortcut dialog, press `Ctrl+S` to be used as the shortcut and click OK.

  5. IntelliJ IDEA will warn you that the shortcut is assigned to another action. Click Remove to remove the `Ctrl+S` shortcut for the Save All action. You can always reassign it later if necessary.

  6. Click OK to apply the changes.




Now, when you press `Ctrl+S`, IntelliJ IDEA will invoke the new macro: reformat the current file and save your project.
