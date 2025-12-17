[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-plugin.html)
[//]: # (Downloaded: 2025-12-17 19:58:40)

## Configuration

Item| Description  
---|---  
VM options| Specify the options to be passed to the Java virtual machine when launching the application, for example, `-mx`, `-verbose`, and so on.When specifying JVM options, follow these rules:

  * Use spaces to separate individual options.
  * If the value of an option includes spaces, enclose either the value or the actual spaces with double quotes.
  * If an option includes double quotes as part of the value, escape the double quotes using backslashes.
  * You can pass environment variable values to custom Java properties.

-Xmx1024m -Dspaces="some arg" -Dmy.prop=\"quoted_value\" -Dfoo=${MY_ENV_VAR} Use code completion in this field: start typing the name of a flag, and the IDE suggests a list of available command line options. This works for `-XX:` and `-X` options and some standard options that are not configured by IntelliJ IDEA automatically, like `-ea`, but not for `-cp` or `–release`.The `-classpath` option specified in this field overrides the classpath of the module.  
Program arguments| Type the list of arguments to be passed to the program, same way as if you were entering these parameters in the command line.Use the same rules as for specifying the [VM options](#vm-options).  
Use classpath of module| Select the module whose classpath should be used to run the application.  
Use alternative JRE| Select this checkbox to enable defining another JRE than the JRE used by the current project / module.  
Show idea.log| If selected, makes IntelliJ IDEA show content of the idea.log file in the console while running the plugin.
