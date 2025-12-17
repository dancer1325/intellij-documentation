[//]: # (Source: https://www.jetbrains.com/help/idea/project-structure-artifacts-java-fx-tab.html)
[//]: # (Downloaded: 2025-12-17 19:56:18)

## JavaFx Application settings

Item| Description  
---|---  
Application class| The qualified application main class name. Normally, this is the class that extends the `javafx.application.Application` class and contains the `main()` method.  
Title| The application title.This is the information for the `<title>` element in the corresponding [deployment descriptor JNLP file](#jnlp).  
Vendor| The name of the application vendor.This information is for the `<vendor>` element in the JNLP file.  
Description| A brief description of the application.This information is for the `<description>` element in the JNLP file.  
Width| The width of the application window in pixels. This parameter is used mainly by the applications embedded in a Web page.  
Height| The height of the application window in pixels. This parameter is used mainly by the applications embedded in a Web page.  
HTML Parameters| You may want to pass dynamic parameters to the application that runs in the Web Start or embedded in browser modes from the [corresponding HTML page](#html). In that case, you should create a .properties file and specify the necessary set of named parameters in that file. Then you should specify the path to the .properties file in this field.  
Application Parameters| You may want to pass named and unnamed parameters to the application. In that case, you should create a .properties file and specify the necessary parameters in that file. Then you should specify the path to the .properties file in this field. (The specified parameters will be included in the [generated deployment descriptor JNLP file](#jnlp).)Example:If the .properties file contains`arg1=value1``arg2`the following elements will be generated within `<jfx:javafx-desc>`:`<fx:param name="arg1" value="value1"/>``<fx:argument>arg2</fx:argument>`  
Update in background| Use this checkbox to set the `check` attribute of the `<update>` element in the JNLP file. (This element is used to specify how Java Web Start should handle the application updates.)If selected, `<update check="background"/>`. The JNLP client will check for updates in the background while the application is being launched.If not selected, `<update check="always"/>`. The JNLP client will always check for updates before launching the application.  
Native bundle| The native bundles to be generated. (A native bundle is an operating system-specific self-contained application package. Such a bundle contains an application itself as well as a JRE, JavaFX runtime and a platform-specific application launcher.)Select:

  * none. No OS-specific bundles are created. The application is packaged into the following files:
    * `<artifact_name>.jar.` This file contains the compiled class files and images.
    * `<artifact_name>.jnlp.` This is a deployment descriptor JNLP file for Web deployment modes (Web Start and embedded in browser).
    * `<artifact_name>.html.` This file contains basic code for running the application in the Web Start and embedded in browser modes.
  * all. All the bundles listed below are generated.
  * deb. A Debian software package for Debian GNU/Linux is generated.
  * dmg. An Apple disk image file for macOS is generated.
  * exe. An executable file for Windows is generated.
  * image. A bundle image for the OS that you are using is generated.
  * msi. A Windows Installer (Microsoft Installer) file is generated.
  * rpm. A Red Hat Package Manager file for Linux is generated.

  
Convert css to bin| Select this checkbox if you want your application CSS file to be converted into the binary format. (This may improve the application performance, especially for "large" CSS files.)  
Enable signing| Select this checkbox if you want the application package to be digitally signed.IntelliJ IDEA can generate a key and the corresponding self-signed certificate, or an existing key may be used to sign the package.To select which way of signing should be used, click Edit Certificates. Then, in the Choose Certificate dialog that opens, select:

  * Self signed. The package will be signed with the generated self-signed certificate.
  * Signed by key. The package will be signed with your private key. Specify the associated settings:
    * Alias. Specify your private key alias.
    * Keystore. Specify the path to the keystore file. (This is where your private key and corresponding certificate are stored.)
    * Storepass. Specify the password for accessing the keystore.
    * Keypass. Specify the password for accessing the key.


