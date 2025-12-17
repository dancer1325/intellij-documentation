[//]: # (Source: https://www.jetbrains.com/help/idea/using-file-and-code-templates.html)
[//]: # (Downloaded: 2025-12-17 20:05:21)

## Syntax

File templates use the [Velocity Template Language](https://velocity.apache.org/) (VTL), which includes the following constructs:

  * Plain text rendered as is.

  * [Variables](file-template-variables.html) that are replaced by their values. For example, `${NAME}` inserts the name provided by the user when adding the file.

  * Various directives, including [#parse](parse-directive.html), `#set`, `#if`, and others.




Start typing `$` or `#` to refer to [completion](auto-completing-code.html) suggestions for available variables and directives.

For more information, refer to the [VTL reference guide](http://velocity.apache.org/engine/2.0/vtl-reference.html).

The following example shows the default template for creating a Java class in IntelliJ IDEA:

#if (${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end #parse("File Header.java") public class ${NAME} { } 

In this template:

  * The `#if` directive checks whether the package name is not empty, and if so, adds the name to the package statement passed as the `${PACKAGE_NAME}` variable.

  * The `#parse` directive [inserts the contents](parse-directive.html) of another template named `File Header.java`, which is available in the Includes tab of the Editor | File and Code Templates settings page `Ctrl+Alt+S`.

  * Then the template declares a public class with the name passed as the `${NAME}` variable (name of the new file).




When you create a new Java file, this template generates a file with contents similar to the following:

package demo; /** * Created by IntelliJ IDEA. * User: John.Smith * Date: 6/1/11 * Time: 12:54 PM * To change this template use File | Settings | File and Code Templates. */ public class Demo { } 
