[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-create-a-live-template-with-variables.html)
[//]: # (Downloaded: 2025-12-17 20:04:41)

# Tutorial: Create a live template with variables and functions

In this tutorial, you will learn how to create and use a simple [live template](using-live-templates.html) that includes [variables](template-variables.html) and [functions](template-variables.html#predefined_functions).

We are going to use the [Spring PetClinic](https://github.com/spring-projects/spring-petclinic) application as a sample project. The resulting live template will:

  * Create a new Java class extending the `Pet` class.

  * Define a String attribute called `food`, where the value is chosen from a list.

  * Implement the `petFood()` method that prints a message.




To get started, [open the Spring PetClinic application](open-close-and-move-projects.html#open-project) in IntelliJ IDEA. If you do not have it locally, clone the application from GitHub:

### Clone the sample project

The source code of the application is hosted on GitHub at <https://github.com/spring-projects/spring-petclinic>.

  1. In the main menu, go to File | New | Project from Version Control.

  2. Specify the URL of the repository and click Clone.

  3. If necessary, agree to open the cloned project in a new window.




Now we will create a new live template. To showcase how variables and functions work in templates, we will add the following variables to the template text:

  * `$ClassName$`: the name of a new class that extends the `Pet` class. It does not have a predefined value, which means that IntelliJ IDEA will prompt you to enter the class name after inserting the template.

  * `$Food$`: a list of three possible values: `meat`, `grass`, and `fruit`. We will use the `enum()` function to define this list. After inserting the template, IntelliJ IDEA will prompt you to choose one of the values in the editor.

  * `$PetName$`: the class name starting with a lowercase letter so that it can be used in a sentence. This demonstrates the use of the `decapitalize()` function applied to another variable.




### Create a live template with variables

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Live Templates.

  2. Select the Java group, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and select Live Template.

  3. In the Abbreviation field, specify the characters that will be used to expand the template. For example, `pet`.

  4. In the Template text field, paste the following template:

type $TypeName$ struct { food string } func (p *$TypeName$) PetFood() { food := "$Food$" println("The $typeName$ eats " + food) } 

class $ClassName$ extends Pet { String food = "$Food$"; public void petFood() { System.out.println("The $PetName$ eats " + food); } } 

![Create a live template](https://resources.jetbrains.com/help/img/idea/2025.3/ij_live_template_example_overview.png)
  5. If there is a No applicable contexts warning, click Define and select Java to make the live template available only in this context. 

  6. Click Edit Variables and, in the Edit Template Variables dialog, configure the variables:

     * `$ClassName$`: leave the Expression field empty. When using the template, IntelliJ IDEA will prompt the user to enter a class name after inserting the template.

     * `$Food$`: in the Expression field, enter `enum("meat","grass", "fruit")`. When using the template, IntelliJ IDEA will display a list of these values in the editor to choose from.

     * `$PetName$`: in the Expression field, enter `decapitalize (ClassName)`. This function converts the first letter of the `$ClassName$` variable value to the lower case.

Select Skip if defined because the value is derived automatically and does not require user input.

![Edit Template Variables](https://resources.jetbrains.com/help/img/idea/2025.3/ij_live_templates_varialbes_example.png)



### Use the created template

  1. In the Project tool window, navigate to the `Owner` package and [create a new Java class](add-items-to-project.html#new-java-class). Specify `Horse` as a class name.

  2. In the editor, start typing the template abbreviation (`pet` in our example) and select it from the completion dropdown.

  3. Enter the class name as a variable value: `Horse`. Press `Tab` to jump to the next variable.

  4. Using the keyboard arrows, select `grass` as a value of the `food` string and press `Enter`.




17 July 2025

[Live template variables](template-variables.html)[Share live templates](sharing-live-templates.html)
