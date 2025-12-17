[//]: # (Source: https://www.jetbrains.com/help/idea/move-members-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:32:47)

# Move Members Dialog

Refactor | Move

`F6`

Move Member refactoring dialog is invoked for static members selected in the Structure view, or in the editor.

Item| Description  
---|---  
Move members from| This read-only field displays the fully qualified name of the source class containing members to be moved.  
To (fully qualified name)| Specify the fully qualified name of the target class.  
Move as enum constant if possible| This option is useful when moving constants (`static final` fields) to an `enum` type in cases when the `enum` type has a constructor with one parameter of the suitable type.Say, we are moving `MOUSE_EVENT` from the class `Events`. class Events { public static final String MOUSE_EVENT = "mouseEvent"; } to the enum `ActionType` enum ActionType { ; String typeName; ActionType(String name) { typeName = name; } } If the option is on, we'll get the following result: enum ActionType { MOUSE_EVENT("mouseEvent"); String typeName; ... } If the option is off, the result will be: enum ActionType { ; public static final String MOUSE_EVENT = "mouseEvent"; String typeName; ... }   
Members to be moved (static only)| This table shows all static members detected in the specified class. Select checkboxes next to the members you want to move.  
Visibility| Specify visibility level. You can either specify it explicitly, or select Escalate to automatically raise it to a necessary level.  
  
28 June 2024

[Move Inner to Upper Level Dialog for Java](move-inner-to-upper-level-dialog-for-java.html)[Move File dialog](move-file-dialog.html)
