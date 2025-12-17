[//]: # (Source: https://www.jetbrains.com/help/idea/compiling-applications.html)
[//]: # (Downloaded: 2025-12-17 19:21:25)

* 💡IntelliJ IDEA native builder 💡
  * allows, about compilation & building process, 
    * compiles source files
    * brings together external libraries + properties files + configurations
    * using the incremental build -- for a -- module or a project
      * -> speeds up the building process 
    * rebuilding a project -- from -- scratch 
    * produce a living application
  * -- based on a -- compiler /
    * works -- according to the -- Java specification
  * use cases
    * pure Java OR Kotlin project 
  * ❌NOT use cases❌  
    * Gradle or Maven project / its build script file uses custom plugins or tasks

* how to compile 1! file OR class?
  * ways
    * way1
      * open the needed file
      * Build > Recompile 'class name'
    * way2
      * open the needed file | Project tool window
      * right-click > Recompile 'class name'

## Change the compilation output locations

* | compile your source code,
  * IntelliJ IDEA AUTOMATICALLY creates an output directory / contains 
    * compiled ".class" files
    * subdirectories / EACH of your modules
      * default paths
        * Sources: <ProjectFolder>/out/production/<ModuleName>
        * Tests: <ProjectFolder>/out/test/<ModuleName>

      ![Compile output directory](https://resources.jetbrains.com/help/img/idea/2025.3/compiler_output.png)

* TODO:
At the project level, you can change the <ProjectFolder>/out part of the output path
If you do so (say, specify some <OutputFolder> instead of <ProjectFolder>/out) but don't redefine the paths at the module level, the compilation results will go to <OutputFolder>/production/<ModuleName> and <OutputFolder>/test/<ModuleName>.

At the module level, you can specify any desirable compilation output location for the module sources and tests individually.

### Specify compilation output folders

  1. Open the Project Structure dialog (File | Project Structure `Ctrl+Alt+Shift+S`).

  2. In Project Settings, select Project and in the Project compiler output field, specify the corresponding path. 

![Project Structure dialog / Projects page](https://resources.jetbrains.com/help/img/idea/2025.3/project_compiler_output.png)

For modules, select Modules, the module you need and the Paths tab. Change the location of the output folder under the Compiler output section.

![Project Structure dialog / Module page](https://resources.jetbrains.com/help/img/idea/2025.3/module_compiler_output.png)


