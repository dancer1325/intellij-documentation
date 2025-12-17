[//]: # (Source: https://www.jetbrains.com/help/idea/analyzing-external-stacktraces.html)
[//]: # (Downloaded: 2025-12-17 19:18:13)

## Analyze Stack Trace dialog

Use this dialog to reach a navigable console stack trace for external applications. From each message in this stack trace, you can navigate right to the source code that cased the reported problem.

Item| Description  
---|---  
Unscramble stack trace| Select this checkbox to unscramble the external stack trace, if your source code is scrambled.  
Unscrambler| Here you can select the unscrambler tool.IntelliJ IDEA ships with the Zelix Klass Master unscrambler plugin. You can develop your own plugin to unscramble stack trace of the code being processed with any other obfuscator.  
Log file| Specify the location of the unscrambler log file.  
Put a stack trace or a complete thread dump here| Paste here the external stack trace or thread dump.  
Automatically detect and analyze thread dumps copied to the clipboard outside of IntelliJ IDEA| If this checkbox is selected, IntelliJ IDEA will monitor and analyze the contents of the clipboard. You can select this checkbox only once, and your clipboard will be scanned every time you switch to IntelliJ IDEA.As soon as something looking like a stack trace gets copied to the clipboard, IntelliJ IDEA will show this stack trace in the corresponding tool window.  
Highlight files changed in last <this_many> days| Select this checkbox to specify the time period in which you want to check last changes in stack traces. The default time period is set to 31 days.  
Normalize| If the stack trace text is corrupted (lines are cut or wrapped, or too long, and so on) after processing with some software (for example, bug tracker or mail client), click this button to restore the normal stack trace structure.
