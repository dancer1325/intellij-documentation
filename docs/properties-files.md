[//]: # (Source: https://www.jetbrains.com/help/idea/properties-files.html)
[//]: # (Downloaded: 2025-12-17 19:56:22)

## Encoding of properties files

In IntelliJ IDEA, the default encoding for properties files is ISO-8859-1. You can also use escape sequences for characters not defined by the selected encoding. Alternatively, you may choose to define a different default encoding for properties files on the project level.

### Configure default encoding for properties files

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Editor | File Encodings.

  2. Select the encoding from the Default encoding for properties files list.

  3. If necessary, enable Transparent native-to-ascii conversion to show native characters (those not defined in [ISO-8859-1](https://en.wikipedia.org/wiki/ISO/IEC_8859-1)) in place of the corresponding escape sequences.




For more information, refer to [Encoding](encoding.html).

If the default encoding for properties files is set to the UTF-8 properties default option in your settings and IntelliJ IDEA encounters a character in the properties file not supported by UTF-8, then IntelliJ IDEA will automatically switch the encoding of that properties file to ISO-8559-1.

![The default properties file encoding setting](https://resources.jetbrains.com/help/img/idea/2025.3/default_properties_file_encoding_setting.png)

If your properties files are using the UTF-8 encoding and IntelliJ IDEA identifies that Java code that is version 8 or earlier (for example, in the runtime of your server) accesses properties files with characters not defined in the ISO-8859-1 character set, the Convert to escape sequences inspection allows you to convert the non-compliant characters into escape sequences for compatibility.

![The convert to escape sequences inspection](https://resources.jetbrains.com/help/img/idea/2025.3/convert_to_escape_sequences.png)
