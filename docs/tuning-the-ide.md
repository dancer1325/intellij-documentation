[//]: # (Source: https://www.jetbrains.com/help/idea/tuning-the-ide.html)
[//]: # (Downloaded: 2025-12-17 20:04:39)

## JVM options

IntelliJ IDEA runs on the Java Virtual Machine (JVM), which has various options that control its performance.

For information about changing JVM options when running the application you are developing in IntelliJ IDEA, see [More options](run-debug-configuration-java-application.html#more_options).

The default options used to run IntelliJ IDEA are specified in the IDE installation directory:

<IDE_HOME>\bin\idea64.exe.vmoptions

IntelliJ IDEA.app/Contents/bin/idea.vmoptions

<IDE_HOME>/bin/idea64.vmoptions

Do not change JVM options in the default file, because it is replaced when IntelliJ IDEA is updated. Moreover, in case of macOS, editing this file violates the application signature.

### Configure JVM options

Do one of the following to create a copy of the default file with JVM options in the [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory) that will override the original file:

  * In the main menu, go to Help | Edit Custom VM Options.

  * If you do not have any project open, on the Welcome screen, click Configure and then Edit Custom VM Options.

  * If you cannot start IntelliJ IDEA, manually copy the default file with JVM options to the IntelliJ IDEA [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).




If you do not have write access to the IntelliJ IDEA configuration directory, you can add the `IDEA_VM_OPTIONS` environment variable to specify the location of the file with your preferred JVM options. This file will override both the original default file and the copy located in the IntelliJ IDEA configuration directory.

If you are using the Toolbox App, it manages the installation and configuration directory and lets you configure JVM options for every IDE instance. Open the Toolbox App, click ![The screw nut icon](https://resources.jetbrains.com/help/img/idea/2025.3/toolbox_settings_screw_icon.png) next to the relevant IDE instance, and select Settings.

### Locate the JVM options file

If you are not sure where IntelliJ IDEA is getting its JVM options, check the following:

  1. The location specified by the `IDEA_VM_OPTIONS` environment variable. If the specified file exists, it will override all other JVM options files.

  2. If the Toolbox App manages your current IntelliJ IDEA instance, open the Toolbox App, click ![The screw nut icon](https://resources.jetbrains.com/help/img/idea/2025.3/toolbox_settings_screw_icon.png) next to the relevant IDE instance, and select Settings. Under Configuration, find Java Virtual Machine options and click Edit.

  3. If you are running a standalone IntelliJ IDEA instance, check the [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

  4. If there are no JVM options files defined in the previous locations, IntelliJ IDEA will use the [default JVM options file](#default-jvm-options). Do not modify it. Use it only to check what are the default options that IntelliJ IDEA uses.




### Common options

The default values of the JVM options should be optimal in most cases. The following are the most commonly modified ones:

`-Xmx`
    

Limits the maximum memory heap size that the JVM can allocate for running IntelliJ IDEA. The default value depends on the platform. If you are experiencing slowdowns, you may want to increase this value, for example, to set the value to 2048 megabytes, change this option to `-Xmx2048m`.

For more information, refer to [Increase the memory heap of the IDE](increasing-memory-heap.html).

`-Xms`
    

Specifies the initial memory allocated by the JVM for running IntelliJ IDEA. The default value depends on the platform. It is usually set to about half of the maximum allowed memory (see [-Xmx](#xmx)), for example, `-Xms1024m`.

`-XX:NewRatio`
    

Specifies the ratio between the size of the young and old generation in the heap. In most cases, a ratio between 2 and 4 is recommended. This will set the size of the young generation to be 1/2 to 1/4 of the old generation correspondingly, which is good when you are often working on one project and only a few files at a time. However, if you are constantly opening new files and switching between several projects, you may need to increase the young generation. In this case, try setting `-XX:NewRatio=1`, which will make the young generation as large as the old generation, allowing objects to remain in the young generation for longer.

For more information, see [Java Garbage Collection Basics](https://www.oracle.com/webfolder/technetwork/tutorials/obe/java/gc01/index.html).

Specify each option on a separate line. Example JVM options file:

-Xmx4G -Xms2G -XX:NewRatio=4 

For more information about the available JVM options, refer to the [java](https://docs.oracle.com/en/java/javase/11/tools/java.html) command reference.
