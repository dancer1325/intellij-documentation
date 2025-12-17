[//]: # (Source: https://www.jetbrains.com/help/idea/compiler.html)
[//]: # (Downloaded: 2025-12-17 19:21:24)

# Compiler

Use this node to configure common options specified in the table below, as well as the specific options for compilers used in IntelliJ IDEA.

Item| Description  
---|---  
Resource patterns| In this field, specify the regular expression that describes the files that should be recognized as resources and, consequently, copied to the output directory. Use semicolons `;` to separate individual patterns.Wildcards and negations are welcome. The following symbols are accepted:

  * `*` represents an unlimited number of any symbols, possibly none.
  * `?` represents exactly one symbol.
  * `.` represents a delimiter.
  * `!` negates the entire mask it is applied to. Consequently, any file with the name and extension that do not match the pattern will be recognized as a resource file.
  * `/` represents a path separator.
  * `/**/` denotes any number of directories.
  * `<dir>:<pattern>` denotes any directory located under the source root `<dir>`; `<pattern>` is any pattern that meets the above-mentioned requirements.

The examples below illustrate the use of wildcards in the resource patterns:

  * `*.xml` \- any XML file.
  * `!*.xml` \- any file whose extension is not .xml.
  * `z*.properties;z*.gif;z*.png;z*.jpeg;z*.xml` \- any .properties, .gif, .png, .jpeg, or .xml file with the name beginning with z.
  * `MyResources:*` \- all files and folders within the directory `MyResources`.

If you want to skip compilation of certain Groovy files in the modules with the Groovy support, include them in the list of the resource patterns.  
Clear output directory on rebuild| Check this option to delete all files in the output directories. Do not check this option, if the output directory contains files IntelliJ IDEA is not aware of, like resources, etc. If there is any intersection of source and output paths, you will be prompted to resolve the issue by separating source and output directories or ignore the issue.  
Add runtime assertions for notnull-annotated methods and parameters| If this option is checked, the assertions are added at runtime to all the methods and parameters, annotated with `@NotNull` annotations. The lists of annotations is [configurable](nullable-notnull-configuration.html) (click the Configure annotations... button to the right).  
Automatically show first error in editor| If this checkbox is selected, the file that contains the first compilation error will be opened in the editor, with the highlighted line that contains the error.  
Display notification on build completion| If this checkbox is selected, the notification balloon is shows if the build process lasts longer than 1 minute. If this build process lasts less than a minute, or if the checkbox is not selected, the message is shown in the [Notifications](notifications.html) tool window and in the Status bar.  
Build project automatically| Select this checkbox to automatically compile the project each time project files change on your disk, for example, on save or autosave, or when you get the latest project revision from your version control system.  
Compile independent modules in parallel| Compile the modules without mutual dependencies simultaneously. Select Enable to always use the parallel compilation or Automatic to use the parallel compilation based on hardware specifications.This option enables faster compilation times for all Maven-based projects compiled by the IDE. This might require increased [heap size](#heap).  
Rebuild module on dependency change| Select this checkbox to have the modules with the changed dependencies fully rebuilt.  
Shared build process heap size (Mbytes)| In the text field, specify the heap size required for the build process.

  * If you are using a 64-bit JDK for compilation, the build process may require more memory.
  * The value is stored with the project settings. If you need to override this value, then in the field User-local build process VM options write `Xmx<N>m`, where `<N>` is the heap size value in megabytes.As soon as this value is recognized in the field User-local build process VM options, the field Shared build process heap size becomes read-only and is ignored.

  
Shared build process VM options| These VM options will be added to the command line on launching the build process. The shared VM options are stored in the project settings and may be put under version control.   
User-local build process VM options (overrides Shared options)| These VM options will be added to the command line on launching the build process. The user-local VM options are stored in workspace.xml file and as such are visible to the author of these changes only. The user-local VM options have the priority over the shared VM options. It means that if anything is written in the field User-local build process VM options, then the field Shared build process VM options is ignored, and the values in the User-local build process VM options field are used instead.  
  
31 October 2024

[Gant settings](gant-settings.html)[Nullable/NotNull configuration dialog](nullable-notnull-configuration.html)
