[//]: # (Source: https://www.jetbrains.com/help/idea/clouds.html)
[//]: # (Downloaded: 2025-12-17 19:20:09)

# Clouds

### Enable the Database Tools and SQL plugin

This functionality relies on the Database Tools and SQL plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

Database Tools and SQL functionality support is limited in IntelliJ IDEA without the Ultimate subscription.

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Database Tools and SQL plugin, and select the checkbox next to the plugin name.




In IntelliJ IDEA, you can work with a database stored in a cloud. To do this, you have to download a cloud provider plugin and connect to your cloud provider account first. IntelliJ IDEA obtains and displays the list of databases available in the account. When you select a database you want to connect to and proceed with creating a data source for it, the connection details are automatically filled in the corresponding files of the Data Sources and Drivers dialog.

Supported clouds and plugins to work with them in IntelliJ IDEA:

  * [Amazon Web Services (AWS)](clouds-aws.html), [AWS Cloud Explorer](https://plugins.jetbrains.com/plugin/28628-aws-cloud-explorer) plugin

  * [Google Cloud Platform (GCP)](clouds-google-cloud.html), [Google Cloud Explorer](https://plugins.jetbrains.com/plugin/28662-google-cloud-explorer) plugin

  * [Azure](clouds-azure.html), [Azure Cloud Explorer](https://plugins.jetbrains.com/plugin/28665-azure-cloud-explorer) plugin




To download a cloud provider plugin and connect to your cloud account, navigate New | Data Source from Cloud Provider and select the plugin to download or cloud you want to connect to.

![Cloud provider submenu in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/cloud_providers_download_menu_azure.png)

All the cloud databases connected to your IDE are displayed in the Cloud tab of the [Data Sources and Drivers dialog](data-sources-and-drivers-dialog.html).

![Cloud tab in the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_cloud_providers_dialog.png)

20 November 2025

[Databases with basic support](other-databases.html)[AWS](clouds-aws.html)
