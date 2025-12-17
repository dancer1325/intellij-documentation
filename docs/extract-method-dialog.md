[//]: # (Source: https://www.jetbrains.com/help/idea/extract-method-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:26)

# Extract Method dialog

For more information about extracting a method and check code examples, refer to the [Extract method](extract-method.html) section.

Item| Description  
---|---  
Name| In this field, specify the name of the function or method to be generated on the basis of the selected source code.  
Visibility| In this area, specify the visibility scope of the method to be generated.  
Declare static| Select this checkbox to have a static method created.If the new method cannot be declared as static, or, vice-versa, can be created only as a static method, the Declare Static checkbox is disabled.  
Generate annotations| This option inserts inferred `@Nullable`/`@NotNull` annotations to parameters and return types.  
Declare varargs| Select this option if you want to declare varargs instead of the array.  
Fold parameters| Select this option to fold the parameters, for example, if you have an array, like `int[] a = new int[i]`, and you want `a[i]` to be passed as a whole to the newly created method.  
Extract chained constructor| Use this option to extract chained constructor from the constructor body, replacing the original code with `this`.  
Output variable(s)| This read-only field displays the name of the variable through which the output of the new method/function will be passed to the calling method/function. Depending on your choice in the [Return output variable(s) through](#returnOutputVariablesThrough) area, this variable either will be used in a return statement or will be declared as the passed by reference parameter of the new method/function.  
Return output variable(s) through| In this area, specify the way in which the new method or function will [return the output variables](http://php.net/manual/en/functions.returning-values.php) to the callee.

  * Return statement \- select this option to have the output variables returned by value. If the Output variable(s) read-only field shows exactly one output variable, it will be used as the return value. If the selection outputs several variables, these variables will be returned as an array.
  * Parameter(s) passed by reference \- select this option to have the output variables returned by reference. IntelliJ IDEA will generate a method/function without a return statement. Instead, the output variables will be added to the set of input parameters in the method/function declaration. The names of these variables will be prepended with an ampersand `&`.

The area is available only when refactoring is invoked in the PHP context.  
Parameters| In this area, select parameters to be passed to the new method/function.If a parameter that is critical for the functionality of the new method is not selected, IntelliJ IDEA will be unable to proceed with the refactoring.  
Move Up/Down| Use these buttons to change the order of the parameters.  
Signature preview| In this read-only field, view the declaration of the new method.  
  
02 September 2025

[Extract Interface dialog](extract-interface-dialog.html)[Extract Method Dialog for Groovy](extract-method-dialog-for-groovy.html)
