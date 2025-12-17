[//]: # (Source: https://www.jetbrains.com/help/idea/maven-repositories.html)
[//]: # (Downloaded: 2025-12-17 19:32:11)

# Maven. Repositories

The table shows the list of [Maven repositories](maven-support.html), encountered in the current project (including repositories in settings.xml), with their URLs, type (local or remote) and the date of the most recent update.

If you need to add a Maven repository, use `pom.xml`. For more information, refer to the [Maven](https://maven.apache.org/guides/introduction/introduction-to-repositories.html) documentation.

Item| Description  
---|---  
Indexed Maven Repositories| This area contains Maven repositories that are configured in the [Effective POM](https://maven.apache.org/plugins/maven-help-plugin/effective-pom-mojo.html) file which lists the default configurations, profiles and goals. IntelliJ IDEA updates the list of repositories automatically. If you open a project that contains additional repositories specified, then the repositories are added to the Indexed Maven Repositories list and you can update the indexes.If you have a problem with your repository, make sure that the indexing service is enabled on the Nexus repository or other repositories you use in your environment.  
Update| Click this button to update indexes of the selected repository. It might be helpful in case you expect to get information for newly deployed artifacts such as new versions of libraries that you use in the project. Also, when you use Maven dependencies completion in pom.xml or generation of Maven dependencies using [Maven Artifact Search](work-with-maven-dependencies.html) dialog. Alternatively, you can use information in [Maven Repositories](maven-projects-tool-window.html#maven_repo) to reindex Maven repositories.  
  
23 October 2024

[Maven. Running Tests](running-tests.html)[Archetype Catalogs](archetype-catalogs.html)
