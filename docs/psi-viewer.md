[//]: # (Source: https://www.jetbrains.com/help/idea/psi-viewer.html)
[//]: # (Downloaded: 2025-12-17 19:56:24)

# PSI Viewer

Tools | View PSI Structure

The PSI Viewer is only available when there is at least one plugin module defined in the project. If you want it to be available for any project, add the following line to the [platform properties file](tuning-the-ide.html#configure-platform-properties): `idea.is.internal=true`

With the PSI viewer, you can explore the internal structure of your source code, as it is interpreted by IntelliJ IDEA.

### View the PSI structure of your source code

  1. From the Tools menu, select View PSI Structure.

  2. In the PSI Viewer dialog, type or paste the fragment of source code to be analyzed in the Text area, select a file type, and specify other options.

     * From the Show PSI structure for list, select the file type or the language construct to be explored. The set of recognized file types depends on the supported languages and installed plugins.

     * Select the Show PsiWhiteSpace checkbox to show the `PsiWhiteSpace` nodes that correspond to the spaces in the source code.

     * In the Text pane, enter the source code to be explored. Type the text manually or paste it from the clipboard. If you have copied some text from the editor, and then open the PSI viewer, the previous contents of the Text pane is selected, which enables you to overwrite it from the clipboard using `Ctrl+V`, or `Ctrl+Shift+V`.

As you enter the code, you can remove line at caret by pressing `Ctrl+Y`, duplicate text with `Ctrl+D`, and add lines using `Shift+Enter`.

  3. Click Build PSI Tree to generate a PSI structure tree view and preview the generated PSI tree in the PSI Structure pane.

If the source code in the Text pane is modified, click Build PSI Tree to refresh the tree view.

Navigating though the tree view highlights the corresponding fragments of source code in the Text pane. If currently selected tree node has references, they are also displayed in the References pane.

The References read-only field shows references to the nodes of the PSI Structure tree view (if any).

Unresolved references are shown red; the corresponding fragments of source code are also highlighted with a red frame.




Item| Description  
---|---  
Show PSI structure for| Use this list to specify file type, or language constructs to be explored. The set of recognized file types depends on the supported languages and installed plugins.  
Show PsiWhiteSpace| If this checkbox is selected, the generated tree view will contain `PsiWhiteSpace` nodes, corresponding to the spaces in the source code. When you select or clear this checkbox, the tree view of the PSI structure changes accordingly.  
Show Tree Nodes|   
Dialect| This list becomes available for the languages that support dialects, for example, SQL, JavaScript and so on.  
Text| Use this pane to enter source code to be explored. IntelliJ IDEA suggests the following ways to supply code:

  * Type immediately within the text area.
  * Paste the text from the clipboard. If you have copied some text from the editor, and then open the PSI viewer, the previous contents of the Text pane is selected, which enables you to overwrite it from the clipboard using `Ctrl+V`, or `Ctrl+Shift+V`.

Note that some editing features are also available: removing line at caret `Ctrl+Y`, duplicating text `Ctrl+D`, and adding line with `Shift+Enter`.  
PSI Structure| This read-only pane displays the PSI structure tree view, generated on clicking the Build PSI Tree button, according to the file type selected in the Show PSI structure for list.Navigating though the tree view highlights the corresponding fragments of source code in the Text pane. If currently selected tree node has references, they are also displayed in the References pane.  
References| This read-only field shows references to the nodes of the PSI Structure tree view (if any).Unresolved references are shown red; the corresponding fragments of source code are also highlighted with a red frame.  
Build PSI Tree| Click this button to generate PSI structure tree view of the code in Text pane, according to the file type selected in the Show PSI structure for list.If the source code in the Text pane is modified, click this button to refresh the tree view.  
  
11 November 2024

[Productivity Guide](productivity-guide.html)[Copy dialog](copy-dialog.html)
