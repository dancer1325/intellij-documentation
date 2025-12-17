[//]: # (Source: https://www.jetbrains.com/help/idea/sbt.html)
[//]: # (Downloaded: 2025-12-17 19:59:44)

# sbt

Use this page to configure the sbt project settings.

Item| Description  
---|---  
General settings  
JVM| Use this area to configure the JVM settings. You can choose from the following options:

  * JRE: select which JDK you want to use in your project. By default, IntelliJ IDEA uses the project's JDK.
  * Maximum heap size, MB: use this field to specify the maximum heap size available to the process that launches the compiler. The default 768 Mb is suitable for most of the purposes.
  * VM parameters: use this field to type the string to be passed to the VM when IntelliJ IDEA launches the compiler. If you need more room to type, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to open the VM parameters dialog where the text entry area is larger.

  
Launcher (sbt-launch.jar)| Use this area to configure settings for the sbt launcher. You can select from the following options:

  * Bundled: use this default option if you want the bundled [sbt launcher](https://www.scala-sbt.org/1.x/docs/Launcher-Getting-Started.html#Getting+Started+with+the+sbt+launcher).
  * Custom: use this option to specify an alternative sbt launcher.

  
sbt projects| Use this area to configure settings for the sbt linked projects.  
Download| 

  * Library sources: select this option to download the Scala library sources.
  * sbt sources: the sbt sources are sources for actual sbt and sbt plugins. Selecting this option might be helpful if you want to debug problems that occurred in your build.

  
Use sbt shell| 

  * for imports: selecting this option might speed up the importing process with less overhead.
  * for builds: by default, the built for the sbt project is run with the IntelliJ IDEA compiler. If you select this option, IntelliJ IDEA will delegate the build process to sbt. In this case, such steps as compilation and source generation are also run within sbt, making the process closer to the actual CI build.

  
Allow overriding sbt version| Select this option to be able to use the latest compatible sbt version in the sbt shell, but not with the regular sbt project import.  
Enable debugging for sbt shell| Select this option if you want to debug code running within the sbt shell. For example, the plugin code or tests that you run from the sbt shell.  
  
11 February 2024

[Build Tools](settings-build-tools.html)[Maven](maven.html)
