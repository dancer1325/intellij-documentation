[//]: # (Source: https://www.jetbrains.com/help/idea/switching-boot-jdk.html)
[//]: # (Downloaded: 2025-12-17 20:03:46)

# Change the boot Java runtime of the IDE

As a Java application, IntelliJ IDEA requires a Java runtime environment (JRE). By default, IntelliJ IDEA uses [JetBrains Runtime](https://github.com/JetBrains/JetBrainsRuntime) (a fork of [OpenJDK](https://github.com/openjdk/jdk)), which is included with the IDE. JetBrains Runtime fixes various known OpenJDK and Oracle JDK bugs, and provides better performance and stability. However, in some cases you may be required to use another Java runtime or a specific version of JetBrains Runtime.

Changing the boot Java runtime may cause unexpected problems. Do not change it unless you were specifically asked to do so by [JetBrains support](https://www.jetbrains.com/support/).

The runtime for IntelliJ IDEA is not the same runtime used for your applications. Define an [SDK](sdk.html) for each of your projects, which includes the necessary development and runtime environment.

### Switch the Java runtime used to run IntelliJ IDEA

  1. In the main menu, go to Help | Find Action or press `Ctrl+Shift+A`.

  2. Find and select the Choose Boot Java Runtime for the IDE action.

  3. Select the new desired runtime and click OK.

If necessary, you can change the location where IntelliJ IDEA will download the selected runtime.

  4. Wait for IntelliJ IDEA to restart with the new runtime.




When you open the Choose Boot Runtime for the IDE dialog for the first time, it may take a while to load the list of JetBrains Runtime builds from the server.

![Choose Boot Runtime for the IDE](https://resources.jetbrains.com/help/img/idea/2025.3/choose-boot-java-runtime-for-ide.png)

To use a different Java runtime available on your computer, select Add Custom Runtime under Advanced in the New field. IntelliJ IDEA lists all the JDKs and JREs that it was able to detect. Select one or click Add JDK to specify the location of the desired Java home directory.

To reset back to the default runtime that the IDE initially used, click Use Default Runtime.

When using a non-default Java runtime for IntelliJ IDEA, it will not update with the IDE and may not be compatible with the new version. Reset back to the default runtime when updating IntelliJ IDEA to get the latest compatible version of JetBrains Runtime.

The path to the selected runtime is stored in the idea.jdk or idea64.jdk file in the IntelliJ IDEA [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory). If there are problems with the selected runtime, you can delete this file to revert to the default runtime.

You can also override the runtime used for IntelliJ IDEA by adding the `IDEA_JDK` environment variable with the path to the desired JDK home directory.

17 February 2025

[Directories used by the IDE](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html)[Increase the memory heap of the IDE](increasing-memory-heap.html)
