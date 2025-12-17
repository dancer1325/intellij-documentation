[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-glassfish-server.html)
[//]: # (Downloaded: 2025-12-17 19:58:05)

## Server tab for a local configuration

Item| Description  
---|---  
Application server| Select the server configuration to be used. Click Configure to create a new server configuration or edit an existing one. (The [Application Servers dialog](application-servers-settings.html) will open.)  
After launch| Select this checkbox to start a web browser after starting the server and deploying the artifacts. Select the browser from the list. Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) `Shift+Enter` to configure your web browsers.  
With JavaScript debugger| If this checkbox is selected, the web browser is started with the JavaScript debugger enabled. Note that JavaScript debugging is available only for Firefox and Google Chrome. When you debug your JavaScript in Firefox for the first time, the JetBrains Firefox extension is installed.  
URL| Specify the URL that the browser should open when the server starts. In most typical cases, this URL corresponds to the root of your Web application or its starting page.  
VM options| Specify the options to be passed to the Java virtual machine when launching the application, for example, `-mx`, `-verbose`, and so on.When specifying JVM options, follow these rules:

  * Use spaces to separate individual options.
  * If the value of an option includes spaces, enclose either the value or the actual spaces with double quotes.
  * If an option includes double quotes as part of the value, escape the double quotes using backslashes.
  * You can pass environment variable values to custom Java properties.

-Xmx1024m -Dspaces="some arg" -Dmy.prop=\"quoted_value\" -Dfoo=${MY_ENV_VAR} Use code completion in this field: start typing the name of a flag, and the IDE suggests a list of available command line options. This works for `-XX:` and `-X` options and some standard options that are not configured by IntelliJ IDEA automatically, like `-ea`, but not for `-cp` or `–release`.The `-classpath` option specified in this field overrides the classpath of the module.  
On 'Update' action| Select the necessary option for the [Update application](updating-applications-on-application-servers.html) function (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg) or `Ctrl+F10` in the Run or Debug tool window). The update options are different for exploded and packed artifacts.For exploded artifacts, the available options are:

  * Update resources. All changed resources are updated (HTML, JSP, JavaScript, CSS and image files).
  * Update classes and resources. Changed resources are updated; changed Java classes (EJBs, servlets, etc.) are recompiled. In the debug mode, the updated classes are hot-swapped. In the run mode, IntelliJ IDEA just updates the changed classes in the output folder. Whether such classes are actually reloaded in the running application, depends on the capabilities of the runtime being used.
  * Redeploy. The application artifact is rebuilt and redeployed.
  * Restart server. The server is restarted. The application artifact is rebuilt and redeployed.

For packed artifacts, the available options are:

  * Hot swap classes. Changed classes are recompiled and reloaded at runtime. This option works only in the debug mode.
  * Redeploy. The application artifact is rebuilt and redeployed.
  * Restart server. The server is restarted. The application artifact is rebuilt and redeployed.

  
Show dialog| Select this checkbox if you want to see the Update dialog every time you use the [Update application](updating-applications-on-application-servers.html) function. The Update dialog is used to select the Update option prior to actually updating the application.  
On frame deactivation| Specify what IntelliJ IDEA should do when you switch from the IDE to a different application (for example, a web browser). (Frame deactivation means switching to a different application.) The options other than Do nothing have the same meanings as in the case of the Update action.  
JRE| By default, the project JDK is used to run the application. If you want to specify an alternative JDK or JRE here, select it from the drop-down list.  
Server Domain| Select the server domain to be used (to deploy and run your application).  
Username| Specify the name of the user on whose behalf IntelliJ IDEA will connect to the server.  
Password| The password of the user specified in the [Username field](#user1).  
Preserve Sessions Across Redeployment| For GlassFish Server 3 or later versions: select this checkbox to preserve active HTTP sessions when redeploying your application artifacts.
