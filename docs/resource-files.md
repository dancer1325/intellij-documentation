[//]: # (Source: https://www.jetbrains.com/help/idea/resource-files.html)
[//]: # (Downloaded: 2025-12-17 19:57:44)

# Resource files

Resources include [properties files](properties-files.html), images, DTDs, and XML files. These files are located in the classpath of your application, and are usually loaded from the classpath using the following methods:

  * `ResourceBundle.getBundle()` for properties files and resource bundles

  * `getResourceAsStream()` for icons and other files




For more information about these methods, refer to [Location-Independent Access to Resources](https://docs.oracle.com/javase/8/docs/technotes/guides/lang/resources.html).

When building an application, IntelliJ IDEA copies all resources into the output directory, preserving the directory structure of the resources relative to the source path. The following file types are recognized as resources by default:

  * .dtd

  * .jpeg

  * .properties

  * .gif

  * .jpg

  * .tld

  * .html

  * .png

  * .xml




The pattern of recognized resource files can be configured as a regular expression in the Compiler dialog (Settings `Ctrl+Alt+S` | Build, Execution, Deployment | Compiler). Using the Resource Patterns field, you can add your own file extensions and create a custom list of resources.

For an example on how to add images to your project, refer to [Example: Import an image](view-images-in-ide.html#import-image-to-project).

31 October 2024

[Non-project files protection](non-project-files-access-dialog.html)[Scratch files](scratches.html)
