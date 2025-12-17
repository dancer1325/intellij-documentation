[//]: # (Source: https://www.jetbrains.com/help/idea/console.html)
[//]: # (Downloaded: 2025-12-17 19:22:24)

## Console common options

Item| Description  
---|---  
Always show debug console| If this checkbox is selected, the debug console will be shown by default in the Debug view.  
Use IPython if available| When the checkbox is selected (by default): If IPython is installed, then IPython console will be launched.If the checkbox is not selected, then, even with the installed IPython, a Python console will be launched.  
Show console variables by default| This checkbox is selected by default to show variables in a console. Deselect it if you do not need to preview variables while working in console.  
Use existing console for "Run with Python console"| If you work in a console and don't want to open a separate Python console when running your Python script, select this checkbox. Your script will be launched in the currently opened console. By default, this option is disabled.  
Command queue for Python Console| Select this checkbox to be able to manage the command execution queue in the Python Console.  
Code completion| Use this drop-down list to select the type of code completion available in the Python console and the Debug Console.Static code completion, which is selected by default, uses the static types, methods, and variables in the source code to provide suggestions.Runtime code completion is based on the runtime state of the application. It uses the types, methods, and variables that are currently active in the memory during the execution of the program.Runtime code completion may lead to certain side effects, such as unintentional code execution without an explicit user input. For example, the class property initialization code will be called immediately after the user enters `.` to get the list of class attributes.To prevent the possible side effects, use static code completion.
