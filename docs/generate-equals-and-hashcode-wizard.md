[//]: # (Source: https://www.jetbrains.com/help/idea/generate-equals-and-hashcode-wizard.html)
[//]: # (Downloaded: 2025-12-17 19:27:26)

# Generate equals() and hashCode() wizard

Use this wizard to [generate equals() and hashCode() methods](generating-code.html#generate-equals-hashcode).

Item| Description  
---|---  
Page1  
Template| Select a predefined velocity template or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to use [Templates dialog](templates-dialog.html).  
For class type comparison in equals() method generate|  Select an expression to generate within the method. Hover over the question mark icon to open a tooltip with an explanation of advantages and disadvantages of using each of the expressions.instanceof expression

  * Allows instances of subclasses to equal instances of the superclass
  * Allows instances of different subclasses to equal each other
  * Avoids extra null check
  * Obeys the Liskov substitution principles

getClass()

  * Overriding the generated equals() method does not break its contract

  
Use getters when available| If this checkbox is selected, the getters are used in `equals()` instead of direct fields access: `getField()` vs `field`.Click Next to open the next page.  
Page 2  
Choose fields to be included in equals()| Select the fields that should be used to determine equality. Each of the selected field's values will be compared, and objects will be considered equal only if all the field values specified here are equivalent.Click Next to open the next page.  
Page 3  
Choose fields to be included in hashCode()| Select the fields to generate hash code. Note that only the fields that were included in the equals() method can participate in creating hash code. All these fields are selected by default, but you can deselect them, if necessary.Click Next to open the next page.  
Page 4  
Select all non-null fields| This page appears if any of the chosen fields are of non-primitive type to avoid generation of unnecessary checks. In other words, if a checkbox for any of these fields is selected, it is presumed that such a field never has a null value and such a check will not be included in generated methods.Click Finish to complete the wizard and create equals() and hashCode() methods.  
  
28 June 2024

[Generate code](generating-code.html)[Templates dialog](templates-dialog.html)
