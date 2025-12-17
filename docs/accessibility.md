[//]: # (Source: https://www.jetbrains.com/help/idea/accessibility.html)
[//]: # (Downloaded: 2025-12-17 19:17:38)

## Set up a screen reader

IntelliJ IDEA fully supports screen readers on both Windows and macOS. 

### Enable a screen reader

  1. Download and enable your preferred screen reader:

     * [NVDA](https://www.nvaccess.org/): use the NVDA 2019.3 or later version for compatibility with 64-bit Java applications, such as IntelliJ IDEA.

Download, install, and enable NVDA.

     * [JAWS](https://www.freedomscientific.com/Products/Blindness/JAWS): use the JAWS 12.0.1158 64-bit or later version for compatibility with 64-bit Java applications, such as IntelliJ IDEA.

Download the version you need and restart your computer to enable the JAWS screen reader.

Enable the [VoiceOver](https://www.apple.com/voiceover/info/guide/_1124.html) screen reader since it is already built into the system.

  2. IntelliJ IDEA automatically shows a prompt suggesting enabling the screen reader support if its installation was detected.

In the dialog that opens, click Enable when you first launch IntelliJ IDEA.

The screen reader support can also be activated later or manually for already installed and configured versions of IntelliJ IDEA.




### Install and set up IntelliJ IDEA

  1. [Download and install](installation-guide.html) IntelliJ IDEA.

For Windows and macOS, when IntelliJ IDEA detects a screen reader on the first launch, it displays a dialog where you can enable a screen reader for IntelliJ IDEA.

  2. To enable screen reader support before the initial launch of IntelliJ IDEA, do the following:

     1. Open the configuration directory that contains personal settings, such as, keymaps, color schemes, and so on.

Syntax
    

%APPDATA%\JetBrains\<product><version>

Example
    

C:\Users\JohnS\AppData\Roaming\JetBrains\IntelliJIdea2025.3

Syntax
    

~/Library/Application Support/JetBrains/<product><version>

Example
    

~/Library/Application Support/JetBrains/IntelliJIdea2025.3

     2. Create a file called idea.properties.

     3. Add the `ide.support.screenreaders.enabled=true` property to the file you have created.

  3. Launch IntelliJ IDEA. The Support screen readers option located in Settings | Appearance & Behavior | Appearance will be enabled.

When the Support screen readers option is enabled, IntelliJ IDEA disables tooltips for icons in the main toolbar, switches controls to a keyboard, and adapts some controls for screen readers.



