[//]: # (Source: https://www.jetbrains.com/help/idea/settings-file-encodings.html)
[//]: # (Downloaded: 2025-12-17 20:01:07)

# File Encodings

IntelliJ IDEA uses these settings to view and edit files for which it was unable to detect the encoding and uses the specified encodings for new files.

![The Editor | File Encodings settings](https://resources.jetbrains.com/help/img/idea/2025.3/settings_editor_file_encodings.png)

If IntelliJ IDEA cannot determine the file or directory encodings, it falls back to the configured project encoding. If there is no project, IntelliJ IDEA uses the global encoding. File or directory encodings take precedence over the project encoding, which, in turn, takes precedence over the global encoding.

For more information about handling file encodings, refer to [Encoding](encoding.html).

Global Encoding
    

Select the encoding to use when other encoding options don't apply.

For example, IntelliJ IDEA will use this encoding for files that are not part of any project or when you check out sources from a version control system.

Project Encoding
    

Select the encoding to use for files that are not listed in the table below.

Path
    

Specify the path to the files or directories for which you want to configure the encoding.

Encoding
    

Select the encoding to use for the specified files and directories.

If this selector is disabled, the file probably has a BOM or declares the encoding explicitly. In this case, you cannot configure the encoding to use for this file.

The encoding selected for a directory applies to all files and subdirectories within it.

Default encoding for properties files
    

Select the encoding for [properties files](properties-files.html) in your project.

In IntelliJ IDEA, the default encoding for properties files is ISO-8859-1. You can also use escape sequences for characters not defined by the selected encoding. Alternatively, you may choose to define a different default encoding for properties files on the project level.

Transparent native-to-ascii conversion
    

Show native characters (those not defined in [ISO-8859-1](https://en.wikipedia.org/wiki/ISO/IEC_8859-1)) in place of the corresponding escape sequences.

![Compare the representation of national characters](https://resources.jetbrains.com/help/img/idea/2025.3/native_to_ascii_conversion.png)

By default, IntelliJ IDEA converts native characters to ASCII escape sequences with uppercase letters. To use lowercase letters, add the following platform property to the custom properties file and restart the IDE:

idea.native2ascii.lowercase=true 

For more information, refer to [Platform properties](tuning-the-ide.html#configure-platform-properties).

Create UTF-8 files
    

Select how IntelliJ IDEA should create [UTF-8](https://en.wikipedia.org/wiki/Byte_order_mark#UTF-8) files:

  * with BOM

  * without BOM

  * with BOM on Window and without BOM otherwise




By default, IntelliJ IDEA creates UTF-8 files without the BOM because some software is not compatible with the BOM, and it may be a problem when interpreting scripts. However, in some cases, you may want to have the BOM in your UTF-8 files.

To add or remove the BOM from all UTF-8 files in your project, select the project folder in the Project tool window. After that, go to File | File Properties and select either Add BOM or Remove BOM.

16 July 2025

[File and Code Templates](settings-file-and-code-templates.html)[Live Templates](settings-live-templates.html)
