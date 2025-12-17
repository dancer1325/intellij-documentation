[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-javascript-debug.html)
[//]: # (Downloaded: 2025-12-17 19:58:14)

## JavaScript Debug-specific configuration settings

Item| Description  
---|---  
URL| 

  * Debugging JavaScript:In this field, specify the URL address of the HTML file that references the JavaScript to debug. For local debugging, type the URL in the format http://localhost:<built-in server port>/<project root>. The built-in server port (1024 or higher) is specified on the [Web Browsers and Preview](settings-tools-web-browsers.html) page of the Settings dialog.
  * Debugging a Dart web application:In this field, specify the URL address of the HTML file that references the Dart code to debug in the format: http://localhost:<built-in server port>/<project-name>/<relative path to the HTML file>. Make sure the port in this URL address is the same as the Built-in server port on the [Web Browsers and Preview](settings-tools-web-browsers.html) page. 

  
Browser| From this list, select Chrome or another browser from the Chrome family where your application will be debugged.For Dart applications, the Dart code will be compiled into JavaScript through the [dart2js](https://dart.dev/tools/dart2js) or [dartdevc](https://dart.dev/tools/dartdevc) tool. The tool is invoked automatically when you [run or debug a Dart web application](dart.html#debug_dart_web_app_webdev_daemon).   
Ensure breakpoints are detected when loading scripts| Select this checkbox to make sure that the breakpoints in the code executed on the page load are hit immediately. Note that this may slow down the initial page load.  
Remote URLs of local files| 

  * Debugging JavaScript:IntelliJ IDEA displays this area only when you create a permanent debug configuration manually. For automatically generated temporary configurations the area is not shown.In this area, map the local files to be involved in debugging to the URL addresses of their copies on the server.
    * File/Directory \- in this read-only field, select the desired local file or directory in the project tree.
    * Remote URL \- in this field, type the absolute URL address of the corresponding file or folder on the server.
These mappings are required only if the local folder structure under the project root differs from the folder structure on the server. If the structures are identical, IntelliJ IDEA itself "retrieves" the paths to local files by parsing the URL addresses of their copies on the server. 
  * Debugging a Dart web application:IntelliJ IDEA displays this area only when the port specified in the URL field is different from the port of the built-in Web server specified on the [Web Browsers and Preview](settings-tools-web-browsers.html) page of the Settings dialog.


