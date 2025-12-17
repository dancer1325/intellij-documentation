[//]: # (Source: https://www.jetbrains.com/help/idea/maven-runner.html)
[//]: # (Downloaded: 2025-12-17 19:32:12)

# Maven. Runner

* goal
  * configure external Maven's settings / used to run goals

Item| Description |  
---|---  |
Delegate IDE build/run actions to Maven | allows: build, run, and debug code -- through -- Maven <br/> uses <br/> &nbsp;&nbsp; configuration / changes the compilation \| fly <br/> &nbsp;&nbsp; build / generates an artifact / custom layout <br/> [Maven projects](delegate-build-and-run-actions-to-maven.md#delegate_to_maven) |  
VM Options| VM options / passed -- to the -- selected JRE <br/> [MORE](#specifyJVMoptionsRulesToFollow) |
JRE | [JRE](maven-support.md#maven_runner_jdk) / used to run the Maven goals |  
Environment variables| This field lets you set custom environment variables on the project level for running maven goals. Specify an environment variable, for example, `${env.JAVA_VERSION}` in the pom.xml of your project.![Environment variable in the pom.xml](https://resources.jetbrains.com/help/img/idea/2025.3/env_var_pom.png)Click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the Environment Variables dialog, where you can set a value for the specified environment variable. For example, `JAVA_VERSION=17`.![Environment Variables dialog](https://resources.jetbrains.com/help/img/idea/2025.3/env_var_dialog.png) |  
Properties| Specify the properties and their values to be passed to Maven |   
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or `Alt+Insert`| Use this icon or shortcut to define a new property as a name - value pair.  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) or `Enter`| Use this icon or shortcut to change the selected property.  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) or `Alt+Delete`| Use this icon or shortcut to remove the selected properties from the list.  
Skip tests| Check this option to skip performing unit tests. This corresponds to the Maven option `-DskipTests=true`.  

## | specify JVM options, rules to follow 

* Use spaces to separate individual options, for example, `-client -ea -Xmx1024m`.
* If an option includes spaces, enclose the spaces or the argument that contains spaces in double quotes, for example, `some" "arg` or `"some arg"`.
* If an option includes double quotes (as part of the argument), escape the double quotes using backslashes, for example, `-Dmy.prop=\"quoted_value\"`.
* You can pass environment variable values to custom Java properties. For example, if you define a variable `MY_ENV_VAR`, you can pass it to the `foo` property as follows: -Dfoo=${MY_ENV_VAR}

28 June 2024

