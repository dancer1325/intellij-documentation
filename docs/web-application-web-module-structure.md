[//]: # (Source: https://www.jetbrains.com/help/idea/web-application-web-module-structure.html)
[//]: # (Downloaded: 2025-12-17 20:06:43)

# Populate Web modules

After you [enable Web development support](enabling-web-application-support.html) in a module, IntelliJ IDEA sets up the basic module structure as follows:

  * Creates a web folder with the index.jsp stub file. By default, the web folder will be the root of your application after deployment and the index.jsp file will be its home page.

  * Creates a WEB-INF subfolder that contains the web.xml descriptor with an `Action` servlet configured.

  * Creates an src folder if you specified so when creating your project.




### Populate the Web module

  * Below the src folder, create the Java class files that implement the functionality of your application.

  * [Configure the static Web content resources](web-application-static-content.html) that represent the user interface.

  * [Configure the application elements](creating-and-configuring-web-application-elements.html).

  * [Specify the assembly descriptor references](specifying-assembly-descriptor-references.html).




17 June 2024

[Enable Web application support](enabling-web-application-support.html)[Configure static content resources](web-application-static-content.html)
