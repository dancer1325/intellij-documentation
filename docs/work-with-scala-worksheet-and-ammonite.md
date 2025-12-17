[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-scala-worksheet-and-ammonite.html)
[//]: # (Downloaded: 2025-12-17 20:07:13)

# Scala worksheet, Scala REPL and Ammonite

You can quickly evaluate and run Scala code using a Scala worksheet, Scala REPL, or [Ammonite](http://ammonite.io/#ScalaScripts).

Scala REPL in IntelliJ IDEA and Scala worksheets both use Scala REPL from the Scala compiler. So, you can use a Scala worksheet instead of Scala REPL to evaluate expressions.

Since in IntelliJ IDEA Scala worksheet and Ammonite files have the same file extension .sc, you need to let IntelliJ IDEA know how to treat such files in your project.

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Languages & Frameworks | Scala.

  2. On the Worksheet tab, in the Treat .sc files as field the Always Worksheet option is selected by default. 

Select Always Ammonite for the Ammonite support.

You can also select the Ammonite in test sources, otherwise Worksheet option to treat only test files as Ammonite.

![Scala worksheet settings](https://resources.jetbrains.com/help/img/idea/2025.3/scala_ws_settings.png)
  3. Save your changes.




While in the settings, you can also set the output cutoff limit, specify in what mode you want to run the worksheet or Ammonite script, or configure how you want IntelliJ IDEA to treat .sc and scratch files.

If you select the Use "eclipse compatibility" mode checkbox then all the statements inside the object will be included in the worksheet's output.

### Create an .sc file

  1. Right-click your project and select New|Scala Worksheet. We recommend that you create an .sc file in the src directory to avoid problems with code highlighting.

  2. In the New Scala Worksheet window, type the name of the file and click OK. 

As a result, a file with .sc extension opens. Based on the [file configuration](#ammonite_settings), it is treated either as a Scala worksheet or as Ammonite.




### Run Scala code using Scala worksheet

  1. Create a [Scala worksheet](#create_sc_file) file and open it in the editor. 

![Scala worksheet](https://resources.jetbrains.com/help/img/idea/2025.3/sc_worksheet.png)
  2. Add your code. 

Besides standard actions such as code completion and string formatting, IntelliJ IDEA supports the following actions:

     * Evaluating Scala objects

     * Folding the output without affecting your code on the left side and expanding only that block of the output that matches a specific statement. 

![Scala worksheet - unfolded results](https://resources.jetbrains.com/help/img/idea/2025.3/sc_wsheet_unfold.png)
  3. Click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) to see the results.




### Start Scala REPL

  1. You can open Scala REPL by pressing. `Ctrl+Shift+D` or you can find it in the Tools menu. 

![Scala REPL in the Tools window](https://resources.jetbrains.com/help/img/idea/2025.3/scala_repl_from_tools.png)

Alternatively, you can open the Actions tab in the Search Everywhere window, start typing Scala REPL, and then select it from the search results. 

![Search Everywhere](https://resources.jetbrains.com/help/img/idea/2025.3/search_everywhere_repl.png)

You can also use a [Scala worksheet](#run_scala_worksheet) to start and work with Scala REPL.

  2. To run a method from your project, import a given class or module, and call it, as if you were writing regular code.

  3. Check the result in the Run tool window.

![Scala REPL](https://resources.jetbrains.com/help/img/idea/2025.3/scala_repl.png)



### Work with the current worksheet settings

  1. Open a Scala worksheet file in the editor. Click ![the Settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) on the toolbar of the worksheet editor to open the Worksheet settings dialog.

  2. In the Worksheet settings dialog, configure the current worksheet settings or the default worksheet settings for the whole project that will affect other worksheets. 

![sc_ws_settings.png](https://resources.jetbrains.com/help/img/idea/2025.3/sc_ws_settings.png)
  3. Use the following options for your configuration: 

     * Interactive Mode: select this checkbox to have the results shown automatically.

     * Make project: clear this check checkbox to disable automatic checking of project's changes and thus improve evaluation performance.

     * Run type: from this list, select the appropriate evaluation mode. For example, select the [REPL](https://docs.scala-lang.org/overviews/repl/overview.html) type to quickly evaluate Scala expressions. When you add new expressions they are executed incrementally.

     * Use class path of module: this field is disabled since the worksheet is a file that you can share between other projects and should stay where you created it. You can change its location in the default settings, but it will be applied across the whole project and will affect other worksheets. 

If you need to change a class path, we recommend that you create and use a [scratch file](scratches.html) instead.

![sc_scratch_file.png](https://resources.jetbrains.com/help/img/idea/2025.3/sc_scratch_file.png)
     * Compiler profile: in this field select a compiler profile for your worksheet. Select one from the list or click ![the Settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) to access the Scala compiler settings for more options. 

If you add or change a profile through the compiler settings, page and you have an [sbt project](sbt-support.html), your changes will be discarded on the next project import.




### Configure the Ammonite support in IntelliJ IDEA

  * Depending on your project, do the following: 

    * If you have an [sbt project](sbt-support.html), add the following code to the  build.sbt  file: 

libraryDependencies += "com.lihaoyi" %% "ammonite" % "2.5.11" % "test" cross CrossVersion.full sourceGenerators in Test += Def.task { val file = (sourceManaged in Test).value / "amm.scala" IO.write(file, """object amm extends App { ammonite.Main.main(args) }""") Seq(file) }.taskValue 

Refresh the project to import the changes.

    * If you have a regular Scala project, download [Ammonite](http://ammonite.io/#Ammonite-REPL) and specify the location of its executable. For example, you can modify the $path variable or specify the path in the default [Ammonite run/debug configuration](run-debug-configuration-ammonite.html), in the Amm executable field.




### Run Scala scripts using Ammonite

  1. Create an [Ammonite file](#create_sc_file) and open it in the editor.

  2. Add your code. 

Besides standard code completion and importing actions, IntelliJ IDEA supports the following Ammonite-specific actions:

     * Code completion for Ammonite-specific commands 

![Ammonite-specific commands](https://resources.jetbrains.com/help/img/idea/2025.3/ammonite_command.png)
     * References to code from other Ammonite files and code completion for them 

![Ammonite file reference](https://resources.jetbrains.com/help/img/idea/2025.3/ammonite_file_reference.png)
  3. In the left gutter, click ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) and select Run script to view the results in the Run tool window. 

Alternatively, you can create and run an [Ammonite run/debug configuration](run-debug-configuration-ammonite.html).




To remove the worksheet's results, click ![the Clear results button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.gc.svg).

To copy your code and evaluation results to the clipboard, click ![the Copy to Clipboard button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg).

26 May 2024

[Run/Debug Configuration: ScalaTest](run-debug-configuration-scala-test.html)[Using ScalaCLI with IntelliJ IDEA](scalacli.html)
