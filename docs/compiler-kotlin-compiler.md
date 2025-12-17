[//]: # (Source: https://www.jetbrains.com/help/idea/compiler-kotlin-compiler.html)
[//]: # (Downloaded: 2025-12-17 19:21:21)

## Common settings

Report compiler warnings| If this checkbox is cleared, the compiler won't generate warnings in course of compilation; only errors and info messages will be left.  
---|---  
Kotlin compiler version| Select the version of the Kotlin compiler that is used to run both local and CI builds.  
Language version| Select the version of Kotlin used by the compiler.  
API version| Select the API version used by the Kotlin compiler.  
Additional command line parameters| Specify the command-line parameters and options to be passed to the compiler at its start. For more information about the available options, refer to the compiler documentation.If you need more room to type, click ![Expand component](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.expandComponent.svg) to open the Additional command line parameters dialog where the text entry area is larger.When specifying the parameters and options, follow these rules:

  * Use spaces to separate individual parameters and options, for example, `-client -ea -Xmx1024m`.
  * If a parameter or an option includes spaces, enclose the spaces or the argument that contains the spaces in double quotes, for example, `some" "arg` or `"some arg"`.
  * If a parameter or an option includes double quotes (e.g. as part of the argument), escape the double quotes by means of the backslashes, for example, `-Dmy.prop=\"quoted_value\"`.

  
Keep compiler process alive between invocations| If this checkbox is selected, the compiler process is always alive.
