[//]: # (Source: https://www.jetbrains.com/help/idea/hibernate-and-jpa-facet-pages.html)
[//]: # (Downloaded: 2025-12-17 19:28:43)

# Hibernate and JPA facet pages

Use this page to manage configuration and object/relational mapping files, and to download missing libraries.

Item| Description  
---|---  
Descriptors| Use the controls in this section to manage configuration and O/R mapping files such as hibernate.cfg.xml for Hibernate, and persistence.xml and orm.xml for JPA. ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) `Alt+Insert`. Add an existing file or create a new one. In the dialog that opens, specify the file location and name.![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) `Enter`. Replace the selected file with another (existing) file. In the dialog that opens, specify the file that you want to use as a replacement.![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) `Alt+Delete`. Remove the selected file from the list. In the dialog that opens, specify whether you want to physically delete the file. (Otherwise, only the file association with the facet will be removed.)  
Default JPA Provider| For JPA: When persistence.xml is created, this setting affects the `<provider>` element in that file. For example, `<provider>org.eclipse.persistence.jpa.PersistenceProvider</provider>` will be generated for EclipseLink. There will be no `<provider>` element if <no provider> is selected.  
Fix| If there are missing libraries, click this button to fix the problem.  
  
11 February 2024

[Facets](facet-page.html)[Java EE Application facet page](java-ee-application-facet-page.html)
