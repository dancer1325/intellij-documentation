[//]: # (Source: https://www.jetbrains.com/help/idea/dependencies-analysis.html)
[//]: # (Downloaded: 2025-12-17 19:24:34)

## Analyze dependencies

  1. In the main menu, go to Code | Analyze Code | Dependencies.

Alternatively, if you want to analyze a specific item, right-click it in the Project tool window and select Analyze | Analyze Dependencies.

  2. In the dialog that opens, specify the scope of files that you want to analyze.

![Selecting the scope of the analysis](https://resources.jetbrains.com/help/img/idea/2025.3/dependency-analysis-scope-dialog.png)

If the necessary scope is not created yet, click ![the Add scope \(Insert\) icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and [define a new scope](configuring-scopes-and-file-colors.html#creating-a-new-custom-scope) in the dialog that opens.

  3. Select the Include test sources option if you want to analyze your test code together with the production code.

  4. Select the Show transitive dependencies option if you want to analyze transitive dependencies and specify the necessary threshold.

For example, A depends on B, and B depends on C. By setting the threshold to 1, the IDE will display B and C dependencies for A. By setting the threshold to 0, only B dependencies will be displayed for A.

  5. Click Analyze to run the analysis.

When the analysis is finished, the results are displayed in the Dependency Viewer tool window.

  6. In the left pane of the tool window, select the node in which you want to search for dependencies.

  7. In the right pane, select the node on which the selected node depends.

Search results are displayed in the lower pane of the tool window. Use the [options](#toolbar1) on the toolbar to manage your search results.

![Dependencies analysis results in the tool window](https://resources.jetbrains.com/help/img/idea/2025.3/analyze-dependencies-results.png)


