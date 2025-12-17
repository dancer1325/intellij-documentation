[//]: # (Source: https://www.jetbrains.com/help/idea/maven.html)
[//]: # (Downloaded: 2025-12-17 19:32:16)

# Maven

On how to install and work with Maven in IntelliJ IDEA, refer to the [Maven support](maven-support.html) section.

Item| Description  
---|---  
Work offline| If this checkbox is selected, Maven works in the [offline mode](working-offline.html#maven) and uses only the resources that are available locally.This option corresponds to the `--offline` command-line option.  
Execute goals recursively| If this checkbox is selected, the build recurses into the nested projects.Clearing this checkbox corresponds to the `--non-recursive` command-line option.  
Print exception stack traces| If this option is checked, exception stack traces are generated.This option corresponds to the `--errors` command-line option.  
Always update snapshots| Select this checkbox if you want IntelliJ IDEA to update snapshots on sync.  
Output level| Select the desired level of the output log, which allows plugins to create messages at levels of _debug_ , _info_ , _warn_ , and _error_ , _fatal_ , or disable output log.  
Checksum policy| Select the desired level of checksum matching while downloading artifacts. You can opt to fail downloading when checksums do not match `--strict-checksums`, or issue a warning `--lax-checksums`.  
Multiproject build fail policy| Specify how to treat a failure in a multiproject build. You can opt to fail the build:

  * At the very first failure, which corresponds to the command line option `--fail-fast`.
  * Fail at the end, which corresponds to the command line option `--fail-at-end`.
  * Ignore failures, which corresponds to the command line option `--fail-never`.

  
Plugin update policy| Select plugin update policy from the list.You can opt for the following:

  * Check for updates, which corresponds to the command line option `--check-plugin-updates`.
  * Suppress checking for updates, which corresponds to the command line option `--no-plugin-updates`.

This option is ignored for Maven 3 and later versions.  
Threads `(-T option)`| Use this field to set the `-T` option for parallel builds. This option is available for Maven 3 and later versions.For more information, refer to [parallel builds in Maven 3](https://cwiki.apache.org/confluence/display/MAVEN/Parallel+builds+in+Maven+3) feature.  
Maven home path| Use this list to select a bundled Maven version that is available (for Maven3, version 3.1 and later) or the result of resolved system variables such as `MAVEN_HOME`. You can also specify your own Maven version that is installed on your machine. You can click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the necessary directory in the dialog that opens.When you open an existing Maven project for the first time, IntelliJ IDEA searches for Maven wrapper defined in .mvn/wrapper/maven-wrapper.properties. If the Maven wrapper is found, it will be used as a Maven home path.The Maven2 version is not bundled with IntelliJ IDEA. If you need to use it in your project, download and enable the [Maven2 support](https://plugins.jetbrains.com/plugin/19663-maven2-support) plugin. Then, [install the needed Maven version locally](maven-support.html#maven2_install).  
User settings file| Specify the file that contains user-specific configuration for Maven in the text field. If you need to specify another file, check Override option, click ellipsis button and select the desired file in the Select Maven Settings File dialog.  
Local repository| By default, the field shows the path to the local directory under the user home, that stores the downloads, and contains the temporary build artifacts that you have not yet released. If you need to specify another directory, check the Override option, click ellipsis button and select the desired path in the Select Maven Local Repository dialog. The selected path will be also displayed in the list of the [indexed Maven repositories](maven-repositories.html#indexed_maven_reps).  
Use settings from .mvn/maven.config| Select this option if you want to use a set of Maven options configured in the [maven.config](https://maven.apache.org/configure.html#mvn-maven-config-file) file for your project. In this case, options that you have in this file will override the same options specified in the Maven settings.For example, if you add an option that is a part of the Maven UI settings to the `maven.config` file, then IntelliJ IDEA will take the value of that option during the next project sync and ignore the one specified in the Maven settings unless the Override checkbox is selected against the options that have this checkbox available.  
  
24 October 2024

[sbt](sbt.html)[Maven. Importing](maven-importing.html)
