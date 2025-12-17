[//]: # (Source: https://www.jetbrains.com/help/idea/encoding.html)
[//]: # (Downloaded: 2025-12-17 19:25:50)

# Encoding

To display and edit files correctly, IntelliJ IDEA needs to know which encoding to use. Source code files are usually encoded in UTF-8. This is the recommended encoding unless you have other requirements.

To determine the encoding of a file, IntelliJ IDEA uses the following steps:

  * If the byte order mark (BOM) is present, IntelliJ IDEA will use the corresponding Unicode encoding regardless of all other settings. For more information, refer to [Byte order mark](https://en.wikipedia.org/wiki/Byte_order_mark).

  * If the file declares the encoding explicitly, IntelliJ IDEA will use the specified encoding. For example, this can apply to XML, HTML, and JSP files. The explicit declaration also overrides all other settings, but you can change it in the editor.

  * If there is no BOM and no explicit encoding declaration in the file, IntelliJ IDEA will use the encoding configured for the file or directory in the [file encoding settings](#file-encoding-settings). If encoding is not configured for the file or directory, IntelliJ IDEA will use the encoding of the parent directory. If the parent directory encoding is also not configured, IntelliJ IDEA will fall back to the Project Encoding, and if there is no project, to Global Encoding.




### Change the encoding used to view a file

If IntelliJ IDEA displays characters in a file incorrectly, it probably couldn't detect the file encoding. In this case, you need to specify the correct encoding to be used for viewing and editing this file.

  1. Open the file in the editor.

  2. Click the File Encoding widget on the [status bar](guided-tour-around-the-user-interface.html#status-bar).

Alternatively, select File | File Properties | File Encoding from the main menu.

  3. Select the correct encoding. 

![Status bar encoding](https://resources.jetbrains.com/help/img/idea/2025.3/encoding2.png)

The list of encodings is rather large. You can use [speed search](speed-search-in-the-tool-windows.html) to quickly find the correct encoding: start typing when the popup is open.

Encodings marked with ![The triangle warning icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.warning.svg) or ![The round error icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.error.svg) might change the file contents. In this case, IntelliJ IDEA opens a dialog where you can choose what to do with the file:

     * Reload: load the file in the editor from disk and apply encoding changes to the editor only. You will see the content changes related to the chosen encoding, but the actual file will not change.

     * Convert: overwrite the file with the chosen encoding.




This will add an association for the file to the [file encoding settings](#file-encoding-settings). IntelliJ IDEA will use the specified encoding to view and edit this file.

### Configure file encoding settings

  * Press `Ctrl+Alt+S` to open settings and then select Editor | File Encodings. 




IntelliJ IDEA uses these settings to view and edit files for which it was unable to detect the encoding and uses the specified encodings for new files. For more information, refer to [File Encodings](settings-file-encodings.html). 

### Select console output encoding

By default, IntelliJ IDEA uses the system encoding to view console output.

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Editor | General | Console.

  2. Select the default encoding from the Default Encoding list.

  3. Click OK to apply the changes.




For more information about console output settings, refer to [Console](settings-console-folding.html).

08 August 2025

[Local History](local-history.html)[Compile and build applications with IntelliJ IDEA](compiling-applications.html)
