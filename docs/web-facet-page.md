[//]: # (Source: https://www.jetbrains.com/help/idea/web-facet-page.html)
[//]: # (Downloaded: 2025-12-17 20:06:47)

# Web facet page

File | Project Structure | Modules | <module> | Web

File | Project Structure | Facets | Web (<module>)

Use this page to edit the settings for your Web facet.

Item| Description  
---|---  
Name| The name of the facet.  
Deployment Descriptors| Form the list of [deployment descriptors](https://en.wikipedia.org/wiki/Deployment_descriptor) for your application.![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) `Alt+Insert`. Create web.xml and add it to the list. The function is not active if the corresponding descriptor is already present in the list.![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) `Alt+Delete`. Remove the selected descriptor from the list.![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) `Enter`. Replace the selected descriptor with another one of the same type.Add Application Server specific descriptor. Create an application server-specific deployment descriptor (for example glassfish-web.xml, jboss-web.xml) and add it to the list.  
Web Resource Directories ![the Web Resource folder](https://resources.jetbrains.com/help/img/idea/2025.3/app.nodes.webFolder.svg)| Specify the directories that contain your web app resources such as web pages, images, etc. (the Web Resource Directory column) and their locations in the corresponding [artifact](working-with-artifacts.html) (the Path Relative to Deployment Root column).For the resource directories to be included in an artifact, you should make sure that the artifact configuration contains a Web facet resources element. (All the resource directories are included in an artifact as a whole.) In that case, / in the Path Relative to Deployment Root column corresponds to the root of that element in the artifact configuration.  
Source Roots| Select the source roots to be included in an [artifact](working-with-artifacts.html). Note:

  * If the '<ModuleName>' compile output element is present in an artifact configuration, the classes for all the source roots are included in the corresponding artifact irrespective of which source roots are selected here.
  * To include only the classes from the source roots selected on this page, use the following when configuring the artifact: ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) | JavaEE Facet Classes | Web (in <ModuleName>). As a result, the corresponding element in the artifact configuration will be shown as '<ModuleName>' module: 'Web' facet classes. 

  
  
11 February 2024

[Java EE Application facet page](java-ee-application-facet-page.html)[Web resource directory path dialog](web-resource-directory-path-dialog.html)
