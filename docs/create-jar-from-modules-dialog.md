[//]: # (Source: https://www.jetbrains.com/help/idea/create-jar-from-modules-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:22:56)

# Create JAR from modules dialog

Use this page to specify the settings for your Java archive (JAR). For more information about creating and running the JAR file, refer to [Create an artifact configuration for the JAR](compiling-applications.html#configure_artifact).

Item| Description  
---|---  
Module| The module that you want to package.  
Main class| The fully qualified name of your main application class, the one with the `main()` method.  
JAR files from libraries| The way the JAR files from the module libraries are processed:

  * extract to the target JAR. The JAR contents are decompressed and then packaged together with the module output in a single JAR.
  * copy to the output directory and link via manifest. The JAR files are copied to the artifact output directory as is. The references to the JARs are added to the `Class-Path` header field of the MANIFEST.MF file that is packaged in the same JAR as the module output.

  
Directory for META-INF/MANIFEST.MF| The path to the directory in which META-INF/MANIFEST.MF is generated. If you build your JAR file with IntelliJ IDEA, IntelliJ IDEA will pick the location to the MANIFEST.MF file automatically. If you use other build systems such as Gradle or Maven, you need to use the resources folder to store the MANIFEST.MF file.  
Include tests| Include the module's compiled test classes.  
  
For more information about creating and building a JAR artifact, refer to [Packaging the application in a JAR](creating-and-running-your-first-java-application.html#package).

11 February 2024

[Choose local paths to upload dialog](choose-local-paths-to-upload-dialog.html)[Create run/debug configuration for Gradle tasks](create-run-debug-configuration-gradle-tasks.html)
