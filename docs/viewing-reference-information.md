[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-reference-information.html)
[//]: # (Downloaded: 2025-12-17 20:06:28)

## Parameter info

The Parameter Info popup shows the names of parameters in method and function calls. IntelliJ IDEA automatically shows a popup with all available method signatures within 1 second (1000 milliseconds) after you type an opening bracket in the editor, or select a method from the suggestion list.

You can explicitly invoke the popup if it has closed or if your IDE is [configured not to show the popup automatically](#configure-parameter-info-popup). To do so, press `Ctrl+P` (or click View | Parameter Info).

![Parameter info popup](https://resources.jetbrains.com/help/img/idea/2025.3/parameter-info.png)

### Show full method or function signatures

By default, the parameter info popup shows simple signatures. You can configure the IDE to show full signatures that include method names and returned types.

  * In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | General | Code Completion, and select the Show full method signatures checkbox.

![Full signatures enabled](https://resources.jetbrains.com/help/img/idea/2025.3/full-signatures.png)



### Configure the parameter info popup

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | General | Code Completion.

  2. In the Show the parameter info popup in ... milliseconds field, specify the time in milliseconds after which the popup should appear. 

If you don't want the popup to appear automatically, clear the Show the parameter info popup in ... milliseconds checkbox.



