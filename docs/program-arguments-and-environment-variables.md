[//]: # (Source: https://www.jetbrains.com/help/idea/program-arguments-and-environment-variables.html)
[//]: # (Downloaded: 2025-12-17 19:56:12)

## Program arguments

  1. Open the [run widget](guided-tour-around-the-user-interface.html#toolbar)'s menu. From the menu, select Edit Configurations.

  2. In the Run/Debug Configurations dialog, open the run configuration, for which you want to modify program arguments.

  3. In the run configuration settings, use the Program arguments field to pass arguments to your application.

!['Program arguments' field in run configuration settings](https://resources.jetbrains.com/help/img/idea/2025.3/ij-add-program-arguments.png)

This is the most common location of the option, which corresponds to run configurations such as Application, Maven, or Spring Boot. The option's exact location and availability might vary depending on the run configuration type.

If you want to use dynamic values from the context, such as the name of the currently opened file, use [macros](#macros).



