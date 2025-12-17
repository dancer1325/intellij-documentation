[//]: # (Source: https://www.jetbrains.com/help/idea/compile-and-build-scala-projects.html)
[//]: # (Downloaded: 2025-12-17 19:21:19)

## Scala compilation settings

By default, you use the Scala compiler(`scalac`) to compile your Scala project. Besides the Scala compiler that supports incremental compilation, you can use the Scala Compile server, which is a Scala compilation subsystem. It helps you reduce the compilation overhead and with the supported parallel compilation can significantly speed up your compilation process. For more information, refer to the [Scala blog post](https://blog.jetbrains.com/scala/2012/12/28/a-new-way-to-compile/).

### Configure compilation settings

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Compiler | Scala Compiler.

  2. On the Scala Compiler page, choose the incremental compiler such as [Zinc](https://www.lightbend.com/blog/zinc-and-incremental-compilation), which is a standalone version of the incremental compiler or the IntelliJ IDEA native one. You can also select the compilation order in which code should be compiled. For example, compile first Scala code and then Java code.

![the Scala Compiler settings](https://resources.jetbrains.com/help/img/idea/2025.3/scala_compiler_settings.png)
  3. Select Scala Compile Server under Scala Compiler to configure the Scala Compile Server.

  4. On the Scala Compile Server page, you can configure the parallel compilation options and the JVM settings. 

![the Scala Compiler Server settings](https://resources.jetbrains.com/help/img/idea/2025.3/scala_compiler_server.png)


