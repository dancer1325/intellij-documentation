[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-scala.html)
[//]: # (Downloaded: 2025-12-17 19:58:47)

## Configuration tab

Item| Description  
---|---  
Program arguments| Type a list of arguments to be passed to the program in the format you would use on the command line. Use the same rules as for specifying the VM options.  
Working directory| Specify the working directory to be used for running the application. This directory is the starting point for all relative input and output paths. By default, the field contains the directory where the project file resides. To specify another directory, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and select the directory.Expand the list to view available [path variables](absolute-path-variables.html) that you can use as a path to your working directory.The list of path variables may vary depending on the enabled plugins.  
Environment variables| Create environment variables and specify their values.   
Use classpath of module| Select the module whose classpath should be used to run the application.  
Add dependencies with “provided” scope to classpath| Enable this option to add dependencies with the Provided scope to the runtime classpath.  
Shorten command line| Select a method that will be used to shorten the command line if the classpath gets too long, or you have many VM arguments that exceed your OS command line length limitation:

  * none: IntelliJ IDEA will not shorten a long classpath. If the command line exceeds the OS limitation, IntelliJ IDEA will be unable to run your application and will display a message suggesting that you specify the shortening method.
  * JAR manifest: IntelliJ IDEA will pass a long classpath via a temporary classpath.jar. The original classpath is defined in the manifest file as a `class-path` attribute in classpath.jar. You will be able to preview the full command line if it was shortened using this method, not just the classpath of the temporary classpath.jar.
  * classpath file: IntelliJ IDEA will write a long classpath into a text file.

  
JRE| By default, the newest JDK from the module dependencies is used to run the application. If you want to specify an alternative JDK or JRE here, select it from the list.
