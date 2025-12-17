[//]: # (Source: https://www.jetbrains.com/help/idea/package-analysis.html)
[//]: # (Downloaded: 2025-12-17 19:33:42)

## Vulnerable dependencies

### Fix vulnerable dependencies in the editor

  1. Open pom.xml or build.gradle in the editor.

The IDE highlights packages that are considered vulnerable.

  2. Place the caret at a highlighted package and press `Alt+Enter` to see the suggested fixes. They may suggest updating to a safe version, visiting the [Mend.io](https://www.mend.io/) website to learn more about a particular vulnerability, or [ignoring](#ignore-vulnerabilities) the vulnerability.


![Change dependency](https://resources.jetbrains.com/help/img/idea/2025.3/change_dependency.png)

### Analyze code to find all vulnerable dependencies

In addition, you can run an inspection to display the list of all declared and imported vulnerable dependencies in the project.

  * In the main menu, navigate to Code | Analyze Code | Vulnerable Dependencies.

  * Alternatively, right-click a folder or a file in the Project tool window `Alt+1` (for example, pom.xml or build.gradle) and select Analyze | Vulnerable Dependencies.




The result is displayed on the Vulnerable Dependencies tab of the Problems tool window (View | Tool Windows | Problems or `Alt+6`) .

![Vulnerable Dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/ij_vulnerable_dependencies_tab.png)

For each vulnerability, you can see an indication of the severity. Click a specific dependency to see more information about the vulnerabilities that were found in that dependency.

To see all project dependencies regardless of whether they are vulnerable or not, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.inspections.inspectionsEye.svg) button on the left panel of the Vulnerable Dependencies tab and select Show Safe Dependencies.

### Ignore vulnerabilities

Ignored vulnerabilities are added to a list in inspection settings. If required, you can share the profile with this list with other members of your team.

  1. Open pom.xml or build.gradle in the editor, place the caret at a highlighted package, and press `Alt+Enter`.

  2. From the list of suggestions, select Ignore vulnerable <package name and version>, and in the dialog that opens, select a reason for ignoring the dependency. Click Ignore.

![Ignoring vulnerability](https://resources.jetbrains.com/help/img/idea/2025.3/ij-ignore-vulnerability.png)



To access the list with ignored vulnerabilities, press `Ctrl+Alt+S` to open the IDE settings and then select Editor | Inspections. Expand the Security node and click Vulnerable declared dependency. The list is located in the Options section in inspection details.

Learn how to share inspection profiles from [Synchronize profiles between computers](customizing-profiles.html#sync-inspection-profiles).
