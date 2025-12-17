[//]: # (Source: https://www.jetbrains.com/help/idea/grammar.html)
[//]: # (Downloaded: 2025-12-17 19:28:24)

## Scope of grammar checks

You can configure the types of files and specific code constructs where you want to check grammar. For example, you can enable grammar checks in Markdown files, in strings and comments of Java files, and disable grammar checks for YAML and JSON.

### Configure where to check grammar

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Natural Languages | Grammar and Style.

  2. On the Scope tab, select the code constructs where you want to check grammar and the types of files for which you want to enable grammar checks.

Option| Description  
---|---  
String literals| Check grammar in string literals.  
Comments| Check grammar in generic line and block comments.  
Documentation| Check grammar in embedded code documentation, such as JavaDoc comments.  
Commit messages| Check grammar in commit messages for the [configured VCS](version-control-integration.html). If you enable this, IntelliJ IDEA adds the corresponding inspection tool to the .idea/vcs.xml configuration file.  
  


