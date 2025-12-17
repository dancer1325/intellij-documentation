[//]: # (Source: https://www.jetbrains.com/help/idea/specifying-compilation-settings.html)
[//]: # (Downloaded: 2025-12-17 20:02:54)

## Supported compilers

Depending on the language you use in your project, you can configure settings for the following compilers:

javac
    

The [Java compiler](java-compiler.html) is taken from the Java SDK currently assigned to the project.

Eclipse
    

IntelliJ IDEA comes bundled with the [Eclipse](java-compiler.html#javac_eclipse) compiler. 

Groovy and Groovy-Eclipse
    

IntelliJ IDEA supports the [groovyc](groovy-compiler.html) for compiling the Groovy part of code in a project. However, you can use the [Groovy-Eclipse](java-compiler.html#groovy_eclipse) compiler if you want to use one process for compiling mixed-language projects.

Kotlin
    

[Kotlin](compiler-kotlin-compiler.html) includes compilers for the supported targets: JVM, JavaScript, and native binaries for [supported platforms](https://kotlinlang.org/docs/reference/native-overview.html#target-platforms).

Scala
    

The Scala compiler is available if the Scala plugin is installed and enabled. You can configure the Scala compiler settings for pure Scala projects as well as for mixed (Scala-Java) projects. You can also configure options for the Scala compiler server.

RMI Compiler
    

The [Java RMI compiler](https://docs.oracle.com/javase/tutorial/rmi/) generates stub and skeleton class files (JRMP protocol) and stub and tie class files (IIOP protocol) for your remote objects.

Gradle-Android Compiler
    

The Gradle-Android compiler lets you compile Gradle-based Android projects.
