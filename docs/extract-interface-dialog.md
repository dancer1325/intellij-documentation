[//]: # (Source: https://www.jetbrains.com/help/idea/extract-interface-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:21)

# Extract Interface dialog

Refactor | Extract Interface

For more information about using [Extract Interface](https://refactoring.guru/extract-interface), refer to the [extract interface](extract-interface.html) section.

Item| Description  
---|---  
Extract interface from| This read-only field shows the source package that contains the class from which the interface will be extracted.  
Extract interface| When selected, IntelliJ IDEA creates a new interface but does not apply it immediately, so the source code remains unchanged.  
Interface name| Enter a name for the new interface. This field is available only if the Extract interface option is selected.  
Extract interface and use it where possible| Select this option to have an interface extracted and immediately applied to the source code, with the suggested changes displayed in the dedicated tab of the [Find](find-tool-window.html) tool window.  
Rename original class and use interface where possible| Use this option to rename the original class and make it an implementation of the newly created interface.  
Rename implementation class to| Type the new name for the original class. The field is available if the Rename original class and use interface where possible option is selected.  
Package for new interface| Specify the package for the new interface. If needed, click the browse icon (![Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg)) and select the package directory.  
Members to Form Interface| Specify the methods of the class, as well as final static fields (constants) to be included in the new interface. To have an element included in the interface, select the checkbox next to it.  
JavaDoc/ASDoc| Specify the action to be applied to the inline documentation. The available options are:

  * As is \- select this option to have the inline documentation left where it is.
  * Copy \- select this option to have the inline documentation copied to the extracted interface without removing it from its current location.
  * Move \- select this option to have the inline documentation moved to the extracted interface and delete it from its current location.

  
  
02 September 2025

[Extract Include File Dialog](extract-include-file-dialog.html)[Extract Method dialog](extract-method-dialog.html)
