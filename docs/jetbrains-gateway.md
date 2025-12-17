[//]: # (Source: https://www.jetbrains.com/help/idea/jetbrains-gateway.html)
[//]: # (Downloaded: 2025-12-17 19:30:25)

# Install JetBrains Gateway

There are several scenarios that can be used to install JetBrains Gateway.

  * You can use IntelliJ IDEA since Remote Development Gateway is a plugin that is bundled by default.

  * You can use JetBrains Toolbox for the JetBrains Gateway installation that manages versions of IntelliJ IDEA and your projects.

  * You can install JetBrains Gateway as a separate launcher.




### Open JetBrains Gateway from your local IntelliJ IDEA

The Remote Development functionality in IntelliJ IDEA relies on the Remote Development Gateway plugin. This plugin comes bundled in IntelliJ IDEA Ultimate by default. If you observe any malfunction, make sure the plugin is enabled.

  1. In your local IntelliJ IDEA, press `Ctrl+Alt+S` to open the IDE settings and select Plugins.

  2. Find the Remote Development Gateway on the Installed tab and make sure that the checkbox next to the plugin name is selected.

  3. From the IntelliJ IDEA welcome screen, click Remote Development.

Alternatively, if you are inside your project, select File | Remote Development from the main menu.

  4. Select the connection type and [follow the suggested steps](remote-development-starting-page.html#start_from_IDE) to connect to a remote server.




### Install JetBrains Gateway via ToolBox

  1. Open the [JetBrains Toolbox App](https://www.jetbrains.com/toolbox-app/). 

![Toolbox](https://resources.jetbrains.com/help/img/idea/2025.3/toolbox_gateway.png)
  2. In the list of products and versions, locate and open Gateway.

  3. Check the prerequisites and connect to a remote server.




### Install JetBrains Gateway manually

  1. Download and run JetBrains Gateway from [JetBrains site](https://www.jetbrains.com/remote-development/gateway/).

Depending on your local OS, use one of the following installers:

Download the [JetBrains Gateway EAP](https://data.services.jetbrains.com/products/download?code=GW&platform=mac&type=eap).dmg.

Download the [JetBrains Gateway release](https://data.services.jetbrains.com/products/download?code=GW&platform=mac&type=release).dmg.

Download the [JetBrains Gateway EAP](https://data.services.jetbrains.com/products/download?code=GW&platform=macM1&type=eap).dmg.

Download the [JetBrains Gateway release](https://data.services.jetbrains.com/products/download?code=GW&platform=macM1&type=release).dmg.

Download the [JetBrains Gateway EAP](https://data.services.jetbrains.com/products/download?code=GW&platform=windows&type=eap).exe.

Download the [JetBrains Gateway release](https://data.services.jetbrains.com/products/download?code=GW&platform=windows&type=release).exe.

Download the [JetBrains Gateway EAP](https://data.services.jetbrains.com/products/download?code=GW&platform=linux&type=eap).tar.gz.

Download the [JetBrains Gateway release](https://data.services.jetbrains.com/products/download?code=GW&platform=linux&type=release).tar.gz.

  2. After the downloading, check the [prerequisites](prerequisites-for-dev-containers.html) and [launch JetBrains Gateway](remote-development-a.html#launch_gateway).




01 April 2025

[Connect to a remote server from IntelliJ IDEA](remote-development-starting-page.html)[Connect and work with JetBrains Gateway](remote-development-a.html)
