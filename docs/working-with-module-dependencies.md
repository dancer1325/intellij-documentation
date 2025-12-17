[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-module-dependencies.html)
[//]: # (Downloaded: 2025-12-17 20:07:26)

## Configure a dependency scope

### Specify a dependency scope

Specifying a dependency scope allows you to control at which step of the build the dependency should be used. The classpath may be different when your sources are compiled, your test sources are compiled, your compiled sources are run, your tests are run.

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S` and click Modules | Dependencies.

  2. Select the necessary scope from the list in the Scope column:

     * Compile: required to build, test, and run a project (the default scope).

     * Test: required to compile and run unit tests.

     * Runtime: included in the classpath for your sources and test sources but only at the run phase.

     * Provided: used for building and testing a project.

  3. The Export option lets you control the compilation classpath for the modules that depend on this one: the marked items will be included in the compilation classpath of the dependent module.


![Configuring dependency scopes](https://resources.jetbrains.com/help/img/idea/2025.3/module-dependencies.png)

IntelliJ IDEA processes dependencies for test sources differently from other build tools (for example, Gradle and Maven).

If your module (say, module A) depends on another module (module B), IntelliJ IDEA assumes that the test sources in A depend not only on the sources in B but also on its own test sources. Consequently, the test sources of B are also included in the corresponding classpaths.

The following table summarizes the classpath information for the possible dependency scopes.

Scope| Sources, when compiled| Sources, when run| Tests, when compiled| Tests, when run  
---|---|---|---|---  
Compile| +| +| +| +  
Test| -| -| +| +  
Runtime| -| +| -| +  
Provided| +| -| +| +
