[//]: # (Source: https://www.jetbrains.com/help/idea/edit-template-variables-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:25:31)

## Controls

Item| Description  
---|---  
Name| In this field, view or edit the variable name in the format `$<variable_name>$`.  
Expression| In this field, specify the expression to have the value of the corresponding template input field calculated automatically.This expression may contain the following constructs:

  * String constants in double quotes
  * Names of other variables defined in a live template
  * [Predefined functions](template-variables.html#predefined_functions) with possible arguments

Type an expression manually or select a predefined function from the list. The list shows also the number and type of parameters, if any, for the selected function. The available functions are listed alphabetically in the [Functions](#predefined_functions) table.  
Default value| In this field, specify the default string to be entered in the corresponding input field of the expanded template, if the expression does not give any result after calculation.Note that a default value of a variable is an expression that can refer to other live template variables. To define the default value as a literal, enclose it in quotation marks.  
Skip if defined| Select this checkbox to have IntelliJ IDEA proceed with the next input field, if the value of the current input field is defined.  
Move Up / Move Down| Use these buttons to change the order of variables in the list. The order of variables in the table determines the order in which IntelliJ IDEA will switch between the corresponding input fields when the template is expanded.
