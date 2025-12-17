[//]: # (Source: https://www.jetbrains.com/help/idea/configure-modules.html)
[//]: # (Downloaded: 2025-12-17 19:21:31)

## Module SDK

An SDK is a collection of tools that you need to develop an application for a specific software framework. To develop Java-based applications, you need a JDK (Java Development Kit).

You can compile a module with an SDK that differs from the project SDK.

### Add a module SDK

  1. In the main menu, go to File | Project Structure | Project Settings | Modules.

  2. Select the module for which you want to set an SDK and click Dependencies.

  3. If the necessary SDK is already defined in IntelliJ IDEA, select it from the Detected SDKs list.

  4. Only for JDKs: if the IDE cannot find the necessary JDK on your computer automatically, click Add JDK from disk and specify its home directory in the dialog that opens.

If you don't have the necessary JDK on your computer, select Download JDK. In the next dialog, specify the JDK vendor, version, change the installation path if required, and click Download.




If you want a module to inherit the project SDK, select the Project SDK option from the Module SDK list.

![Setting up another module-level SDK](https://resources.jetbrains.com/help/img/idea/2025.3/sdks_project_structure_modules_dependencies.png)

### How does IntelliJ IDEA know which JDK to use?

IntelliJ IDEA does the following to determine which JDK to use for compilation if you use different JDKs for modules in your project.

  * It checks all JDKs that are used in the project: the JDKs that are defined on both the project and module levels.

  * It calculates the latest of these JDKs. This is necessary to make sure all modules can be compiled.

  * If the version of the latest JDK configured is lower than 1.6, IntelliJ IDEA will pick the JDK version that is used for running the IDE. This limitation is related to the fact that the compiler API used by IntelliJ IDEA for building projects is supported starting from JDK 1.6.

  * Although a specific version of the compiler will be used (in accordance with the selected JDK version), each separate module will be compiled using the javac's cross-compilation feature against the libraries of the JDK defined for this particular module in the project settings.

This protects you from a situation when a module is compiled against newer libraries than those for which dependencies are set.



