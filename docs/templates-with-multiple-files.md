[//]: # (Source: https://www.jetbrains.com/help/idea/templates-with-multiple-files.html)
[//]: # (Downloaded: 2025-12-17 20:04:07)

## Example: Template for the MVC pattern

Let's say you want to implement the [MVC](https://en.wikipedia.org/wiki/Model-view-controller) pattern in your application. This means you need separate files for the data layer (model), the presentation layer (view), and the controller that performs all interactions between the model and the view. This tutorial shows how you can add a template that creates all three files at once.

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Editor | File and Code Templates.

  2. Create the data model class template.

On the Files tab, click ![the Create Template button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and specify the following:

     * Name: `Java MVC`

     * Extension: `java`

     * File name: `${NAME}`

Add the following code to the template body:

public class ${NAME} { // This is the data model } 

The name of this class will match the name that you provide, for example: `Counter`.

An instance of this class instance might store the data in its fields or access a database. Depending on your needs, you can expand this template to include boilerplate methods (perhaps, getters and setters) or import statements for a persistence framework.

  3. Create the view class template.

Select the new Java MVC template in the list and click ![The Create Child Template File button](https://resources.jetbrains.com/help/img/idea/2025.3/app.fileTypes.addAny.svg) on the toolbar. Specify the following:

     * File name: `${NAME}View`

     * Extension: `java`

Add the following code to the template body:

public class ${NAME}View { // This is the user interface } 

The name of this class will be a combination of the name that you provide and the word `View`, for example: `CounterView`.

If it's a CLI application, you can define methods that print the application's output and scan the user's input through the standard system input and output streams.

If it's a GUI application, you can use Swing, JavaFX, or some other GUI framework. In this case, you can include necessary import statements and boilerplate code in the template.

For a web application, the view can be a JSP page. In this case, you need to create it under the webapp directory. Set File name to `webapp/${NAME}View` and Extension to `jsp`.

  4. Create the controller class template.

Select the Java MVC template in the list and click ![The Create Child Template File button](https://resources.jetbrains.com/help/img/idea/2025.3/app.fileTypes.addAny.svg) on the toolbar. Specify the following:

     * File name: `${NAME}Controller`

     * Extension: `java`

Add the following code to the template body:

public class ${NAME}Controller { private ${NAME} model; private ${NAME}View view; public ${NAME}Controller(${NAME} m, ${NAME}View v) { this.model = m; this.view = v; } // This is the logic for interacting between the model and the view } 

The name of this class will be a combination of the name that you provide and the word `Controller`, for example: `CounterController`.

For a web application, the controller might be a Servlet class. In this case, add the necessary `javax.servlet` imports to your template, the `@WebServlet` annotation, extend the class from `HttpServlet`, and provide the necessary boilerplate methods.

  5. Click OK to apply the changes.

  6. To use the new template, right-click a directory in the Project tool window or press `Alt+Insert` and select the Java MVC template. Specify a name for the model class, and IntelliJ IDEA will create all three files.


![Example of using Live Templates](https://resources.jetbrains.com/help/img/idea/2025.3/mvc-multiple-file-template.png)
