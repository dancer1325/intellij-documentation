[//]: # (Source: https://www.jetbrains.com/help/idea/hard-coded-string-literals.html)
[//]: # (Downloaded: 2025-12-17 19:28:39)

## Internationalize Hardcoded String dialog

IntelliJ IDEA provides a special intention action i18nize hard coded string literal to extract string literals into your properties files. You can access the resource bundle using either the [java.util.ResourceBundle class](#extract-using-java.util.ResourceBundle) or a custom utility class.

Item| Description  
---|---  
Properties file| In this field, specify an existing .properties file to store the extracted string literal. Type the path to the file manually or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the Choose Properties File dialog, where you can select the desired location using the project tree view or through a search by name.  
Update all properties files in resource bundle| Select this checkbox to have all properties files in the target bundle updated.  
Property key| By default, this field displays the suggested key name, based on the value of the string to be extracted. Keep the default name or type the desired one.  
Property value| By default, this field displays the value of the string to be extracted. Keep the default value or type the desired one.  
Resource bundle expression| By default, this field displays a resource bundle expression from the resource bundle declaration in the source code. If the resource bundle is not declared in the source code, the field does not appear. To define the desired expression, do one of the following: 

  * Enter an expression of the ResourceBundle type, as described in the section [Extract a string literal using java.util.ResourceBundle](#extract-using-java.util.ResourceBundle).
  * Use your own custom utility class.

Basic code completion `Ctrl+Space` is available in this field.  
Edit i18n template| Click this link to open the Edit File Template dialog, where you can change the I18nized Expression template to point to the method of a custom utility class that will be used to access a resource bundle. For more information, refer to [Edit the internationalized expression template](#edit-internationalized-expression-template). A changed file template is a global setting that affects all projects. If you want to restore defaults, open the [File and Code Templates](settings-file-and-code-templates.html) dialog, find the I18nized Expression template in the Code tab, and click the Reset button ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.rollback.svg).  
Preview| This read-only field displays the results of applying the I18nize hard-coded string literal intention action.
