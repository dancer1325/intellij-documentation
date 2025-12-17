[//]: # (Source: https://www.jetbrains.com/help/idea/go-workspaces.html)
[//]: # (Downloaded: 2025-12-17 19:28:18)

# Go workspaces

Go workspaces help you manage multiple modules within a single project. When you create a go.work file, Go reads the list of modules defined in the workspace and generates a unified list of dependencies. If any go.mod files include `replace` directives, they are also taken into account. This combined dependency list is then applied to all modules in the workspace.

When you create a go.work file, IntelliJ IDEA automatically includes all modules in the current project.

### Create a workspace

  * Right-click the parent directory of your project. Then select New | Go Workspace File.




You can also generate a go.work file from an existing `go.mod` file if it contains `replace` directives.

### Merge several use directives into one directive

  * Click a `use` directive, press `Alt+Enter`, and select Merge multiple 'use' directives into one.




03 April 2025

[Go tools](integration-with-go-tools.html)[Go templates](integration-with-go-templates.html)
