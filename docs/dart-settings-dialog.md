[//]: # (Source: https://www.jetbrains.com/help/idea/dart-settings-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:23:53)

# Dart settings

Item| Description  
---|---  
Enable Dart support in project <project name>| 

  * When this checkbox is selected, IntelliJ IDEA provides assistance in coding, testing, running, and debugging Dart applications and enables you to configure the Dart SDK.
  * When the checkbox is cleared, no assistance in developing Dart applications is provided and all the controls on the page are disabled.

  
Dart SDK path| In this field, specify the location of the downloaded Dart SDK. If you followed the standard installation procedure, as described on the [Dart official website](https://dart.dev/get-dart), IntelliJ IDEA detects the path to the Dart SDK automatically.Alternatively, type the path manually or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the path in the dialog that opens.If IntelliJ IDEA recognizes the Dart SDK correctly, its revision number is displayed in the Version read-only field.  
Version| In this read-only field, IntelliJ IDEA shows the revision number of the detected Dart SDK, provided that the SDK is recognized correctly.  
Check SDK update| When this checkbox is selected, IntelliJ IDEA checks whether the specified above version of SDK is the latest one. If a newer version of SDK is available, IntelliJ IDEA displays a pane at the top of the active editor informing you that a newer SDK version has been released. Do one of the following:

  * Click the Download SDK link and download it from the site.
  * If you have already downloaded the latest SDK version, click the Dart Settings link to switch to the Dart page of the Settings dialog and specify the new SDK location.

From the list, choose the release types of SDK to look in. The available options are:

  * Stable channel
  * Stable and Dev channels

  
Webdev server port| In this field, specify the port on which the [webdev server](https://dart.dev/tools/webdev#serve) will start the Dart web app, refer to [Running and debugging Dart web applications](dart.html#debug_dart_web_app_webdev_daemon).If you are debugging your Dart web application with Dart webdev daemon, configure the port in the [Dart Web run/debug configuration](run-debug-configuration-dart-web.html), refer to [Running and debugging Dart web applications](dart.html#debug_dart_web_app_webdev_daemon).The default webdev server port is 53322. If this port is already busy, IntelliJ IDEA uses the closest free one.   
  
11 February 2024

[Dart](dart.html)[Dart Analysis tool window](dart-analysis-tool-window.html)
