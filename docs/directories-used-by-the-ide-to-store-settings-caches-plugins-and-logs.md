[//]: # (Source: https://www.jetbrains.com/help/idea/directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html)
[//]: # (Downloaded: 2025-12-17 19:25:01)

## Configuration directory

The IntelliJ IDEA configuration directory contains user-defined IDE settings, such as keymaps, color schemes, custom [VM options](tuning-the-ide.html#configure-jvm-options), [platform properties](tuning-the-ide.html#configure-platform-properties), and so on.

Syntax
    

%APPDATA%\JetBrains\<product><version>

Example
    

C:\Users\JohnS\AppData\Roaming\JetBrains\IntelliJIdea2025.3

Syntax
    

~/Library/Application Support/JetBrains/<product><version>

Example
    

~/Library/Application Support/JetBrains/IntelliJIdea2025.3

Syntax
    

~/.config/JetBrains/<product><version>

Example
    

~/.config/JetBrains/IntelliJIdea2025.3

You can change the location of the IntelliJ IDEA configuration directory using the [idea.config.path](#idea.config.path) property.

To share your personal IDE settings, copy the files from the configuration directory to the corresponding folders on another IntelliJ IDEA installation. Make sure that IntelliJ IDEA is not running to avoid erasing the copied files when you shut down the IDE. Depending on which settings you modified, the IntelliJ IDEA configuration directory can contain the following subfolders: 

Directory| User settings  
---|---  
codestyles| Customized [code style schemes](configuring-code-style.html)  
colors| Customized [editor color and font schemes](configuring-colors-and-fonts.html)  
fileTemplates| User-defined [file templates](using-file-and-code-templates.html)  
filetypes| User-defined [file types](creating-and-registering-file-types.html)  
inspection| [Code inspection profiles](code-inspection.html)  
keymaps| Customized [keyboard shortcuts](configuring-keyboard-and-mouse-shortcuts.html)  
migration| Predefined and user-defined [migration maps](migrate.html)  
options| Various options, for example, feature usage statistics and macros  
scratches| [Scratch files and buffers](scratches.html)  
settingsSync| IDE settings shared using [Backup and Sync](sharing-your-ide-settings.html#IDE_settings_sync)  
templates| User-defined [live templates](using-live-templates.html)  
tools| Configuration files for [user-defined external tools](configuring-third-party-tools.html)
