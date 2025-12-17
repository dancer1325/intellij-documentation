[//]: # (Source: https://www.jetbrains.com/help/idea/artifacts.html)
[//]: # (Downloaded: 2025-12-17 19:18:32)

# Artifacts

For more information about working with artifacts, refer to [Artifacts](working-with-artifacts.html).

![Project Structure dialog / Artifacts page](https://resources.jetbrains.com/help/img/idea/2025.3/project_structure_artifacts.png)

Name| The name of the artifact configuration and also that of the artifact.  
---|---  
Type| The artifact type. Defines the artifact format and structure, highlighting of problematic parts in the artifact layout as well as the options that IntelliJ IDEA suggests (or assumes acceptable) in relation to the artifact composition.  
Output directory| The artifact, when built (Build | Build Artifacts), is placed into the directory whose path is specified in this field.If the artifact is not going to be used on its own but only as a part of other artifacts, the field may be left empty. In this case, the artifact will not appear in the suggestion list on choosing Build | Build Artifacts and no target will be generated for it in build.xml on choosing Build | Generate Ant Build.  
Include in project build| Build the artifact automatically when building the project (Build | Build Project).  
  
11 October 2024

[Libraries and global libraries](libraries-and-global-libraries.html)[Output Layout tab](output-layout-tab.html)
