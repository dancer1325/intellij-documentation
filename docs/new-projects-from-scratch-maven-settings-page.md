[//]: # (Source: https://www.jetbrains.com/help/idea/new-projects-from-scratch-maven-settings-page.html)
[//]: # (Downloaded: 2025-12-17 19:33:03)

# New project wizard. Maven settings page

This page appears when you select [Create from archetype](maven-support.html#maven_archtype_settings) option in the [project wizard for Maven](maven-support.html#create_new_maven_project). Use this page to modify Maven default settings.

To open [Maven Settings dialog](maven.html) after you opened your project, refer to the [accessing Maven settings](maven-support.html#maven_settings_access).

Item| Description  
---|---  
Maven home directory| Use this list to select a bundled Maven version that is available (for Maven2, version 2.2.1 and for Maven3, version 3.1) or the result of resolved system variables such as `MAVEN_HOME` or `MAVEN2_HOME`. You can also specify your own Maven version that is installed on your machine. You can click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the necessary directory in the dialog that opens.  
User settings file| Specify the file that contains user-specific configuration for Maven in the text field. If you need to specify another file, select Override checkbox, click the ellipsis button and select the desired file in the Select User Settings File dialog.  
Local repository| By default, this field shows the path to the local directory under the user home that stores downloads and contains the temporary build artifacts that you have not yet released. If you need to specify another directory, select Override checkbox, click the ellipsis button and select the desired path in the Select Local Repository dialog.  
Properties| By default, the columns in this area display system properties that are passed to Maven for creating a project from the archetype.You can click the following buttons to modify displayed properties:

  * ![Add Maven property](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add a Maven property.
  * ![Delete Maven property](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) Remove a Maven property.
  * ![Edit Maven property](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) Edit a Maven property.

  
  
28 June 2024

[New Project: Bootstrap](create-new-project-twitter-bootstrap.html)[Build tool window](build-sync-tool-window.html)
