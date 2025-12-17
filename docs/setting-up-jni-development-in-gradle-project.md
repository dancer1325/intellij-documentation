[//]: # (Source: https://www.jetbrains.com/help/idea/setting-up-jni-development-in-gradle-project.html)
[//]: # (Downloaded: 2025-12-17 20:00:23)

# Set up JNI development in Gradle project

IntelliJ IDEA supports [JNI development in Gradle](https://docs.gradle.org/current/userguide/native_software.html) projects.

This tutorial uses on the Java 1.8 and Gradle 7.4 versions. The tutorial uses the [software model](https://blog.gradle.org/state-and-future-of-the-gradle-software-model). 

If you want to use the [replacement plugins](https://docs.gradle.org/current/userguide/building_cpp_projects.html#cpp_plugin), you can check the [JNI Sample](https://github.com/vladsoroka/GradleJniSample) project.

If you use Kotlin in your project, check out the [Kotlin tutorial](https://kotlinlang.org/docs/get-started-with-jvm-gradle-project.html).

### To add JNI support

  1. Create a [new](gradle.html#project_create_gradle) or open an [existing](gradle.html#gradle_import) Gradle project.

  2. Open the build.gradle file.

  3. Add the following code to the build.gradle:

import org.gradle.internal.jvm.Jvm plugins { id 'java' id 'application' id 'c' } mainClassName = 'HelloWorld' repositories { mavenCentral() } dependencies { testImplementation 'junit:junit:4.12' } sourceCompatibility = 1.8 targetCompatibility = 1.8 application { applicationDefaultJvmArgs = ["-Djava.library.path=" + file("${buildDir}/libs/hello/shared").absolutePath] } model { platforms { x64 { architecture "x86_64" } } components { hello(NativeLibrarySpec) { targetPlatform "x64" binaries.all { def jvmHome = Jvm.current().javaHome if (targetPlatform.operatingSystem.macOsX) { cCompiler.args '-I', "${jvmHome}/include" cCompiler.args '-I', "${jvmHome}/include/darwin" cCompiler.args '-mmacosx-version-min=10.4' linker.args '-mmacosx-version-min=10.4' } else if (targetPlatform.operatingSystem.linux) { cCompiler.args '-I', "${jvmHome}/include" cCompiler.args '-I', "${jvmHome}/include/linux" cCompiler.args '-D_FILE_OFFSET_BITS=64' } else if (targetPlatform.operatingSystem.windows) { cCompiler.args "-I${jvmHome}/include" cCompiler.args "-I${jvmHome}/include/win32" } else if (targetPlatform.operatingSystem.freeBSD) { cCompiler.args '-I', "${jvmHome}/include" cCompiler.args '-I', "${jvmHome}/include/freebsd" } } } } } classes.dependsOn 'helloSharedLibrary' 

import org.gradle.internal.jvm.Jvm plugins { id 'java' id 'application' id 'c' } mainClassName = 'HelloWorld' repositories { mavenCentral() } dependencies { testImplementation 'junit:junit:4.12' } sourceCompatibility = 1.8 targetCompatibility = 1.8 application { applicationDefaultJvmArgs = ["-Djava.library.path=" + file("${buildDir}/libs/hello/shared").absolutePath] } model { platforms { x64 { architecture "x86_64" } } components { hello(NativeLibrarySpec) { targetPlatform "x64" binaries.all { def jvmHome = Jvm.current().javaHome if (targetPlatform.operatingSystem.macOsX) { cCompiler.args '-I', "${jvmHome}/include" cCompiler.args '-I', "${jvmHome}/include/darwin" cCompiler.args '-mmacosx-version-min=10.9' linker.args '-mmacosx-version-min=10.9' linker.args '-stdlib=libc++' } else if (targetPlatform.operatingSystem.linux) { cCompiler.args '-I', "${jvmHome}/include" cCompiler.args '-I', "${jvmHome}/include/linux" cCompiler.args '-D_FILE_OFFSET_BITS=64' } else if (targetPlatform.operatingSystem.windows) { cCompiler.args "-I${jvmHome}/include" cCompiler.args "-I${jvmHome}/include/win32" } else if (targetPlatform.operatingSystem.freeBSD) { cCompiler.args '-I', "${jvmHome}/include" cCompiler.args '-I', "${jvmHome}/include/freebsd" } } } } } classes.dependsOn 'helloSharedLibrary' 

To make your setup work smoothly, keep in mind the following details :

     * IntelliJ IDEA uses the version of Gradle JVM located in the [Gradle settings](gradle-settings.html#gradle_jvm).

     * Depending on your OS, compiler parameters may vary, keep that in mind when you change `cCompiler.args` and `linker.args` in your build.gradle.

     * When the application is run with the following existing system property:

application { applicationDefaultJvmArgs = ["-Djava.library.path=" + file("${buildDir}/libs/hello/shared").absolutePath] } 

and this application depends on `classes.dependsOn 'helloSharedLibrary'`, IntelliJ IDEA generates the binary libhello.dylib file for the shared library in the Project tool window.

![binary for shared library](https://resources.jetbrains.com/help/img/idea/2025.3/binary_for_shared_library.png)

Note that libhello.dylib depends on the OS you have. For example, for Windows the name of the binary will be hello.dll.

  4. In the Project tool window, select the src | java directory.

  5. Right-click the java directory and select New | Java Class to create a Java class `HelloWorld` that will use `C` code.

  6. Open the created `HelloWorld` class in the editor and enter the following code: 

class HelloWorld { public native void print(); static { System.loadLibrary("hello"); } public static void main(String[] args) { new HelloWorld().print(); } } 

Code specified in the file will load the generated [system library](#library_binary).

  7. In the Project tool window, in the src directory, create the hello/c/hello.c file, which is a file for your `C` programs.

  8. Open the hello.c file in the editor and specify the following code: 

#include <jni.h> #include <stdio.h> JNIEXPORT void JNICALL Java_HelloWorld_print(JNIEnv *env, jobject obj) { printf("Hello From C++ World!\n"); return; } 




At this point you can start developing your application further using native codes as needed.

### Run your application

  1. Open your run configuration dialog.

  2. If you use macOS as your operating system, then add the following code to the VM options field.

![Run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/run_config_vm_options.png)

The VM options field can be added from the Modify options list.

Click OK to save the changes.

  3. Click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.runConfigurations.testState.run.svg) on the main toolbar.




28 June 2024

[Publish a Java library to a Maven repository](add-a-gradle-library-to-the-maven-repository.html)[Getting started with Ant](ant.html)
