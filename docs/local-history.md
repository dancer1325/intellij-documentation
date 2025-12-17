[//]: # (Source: https://www.jetbrains.com/help/idea/local-history.html)
[//]: # (Downloaded: 2025-12-17 19:31:34)

## Location of Local History files

Local History is stored as binary files under the LocalHistory  subdirectory in the [IntelliJ IDEA system directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#system-directory):

Syntax
    

%LOCALAPPDATA%\JetBrains\<product><version>

Example
    

C:\Users\JohnS\AppData\Local\JetBrains\IntelliJIdea2025.3

Syntax
    

~/Library/Caches/JetBrains/<product><version>

Example
    

~/Library/Caches/JetBrains/IntelliJIdea2025.3

Syntax
    

~/.cache/JetBrains/<product><version>

Example
    

~/.cache/JetBrains/IntelliJIdea2025.3

You can change the location of the system directory using the [idea.system.path](tuning-the-ide.html) property.
