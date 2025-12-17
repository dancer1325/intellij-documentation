[//]: # (Source: https://www.jetbrains.com/help/idea/file-and-project-analysis.html)
[//]: # (Downloaded: 2025-12-17 19:26:48)

## Current file

The IDE continuously checks your code and searches for problems. The widget in the top-right corner of the editor displays the number of problems of each [severity](configuring-inspection-severities.html) detected in the current file:

![Inspection widget](https://resources.jetbrains.com/help/img/idea/2025.3/ws_inspection-widget.png)

The widget has a simplified view. To enable it, hover over the widget, click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg), and select Compact View.

Click the widget to open the list of problems in the File tab of the [Problems tool window](problems-tool-window.html). You can also access the Problems tool window by selecting View | Tool Windows | Problems or by pressing `Alt+6`.

For each problem, you can see the suggested quick-fix by pressing `Alt+Enter` or by clicking ![Show Quick Fixes](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.codeInsight.intentionBulb.svg). To jump to the corresponding line in the editor, press `F4` or double-click the problem in the tool window. 

Click ![Open Editor Preview](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.previewVertically.svg) to be able to view and fix problems right in the tool window. 

![File tab in Problems tool window](https://resources.jetbrains.com/help/img/idea/2025.3/problems-toolwindow-reference.png)

The color stripe in the scrollbar also marks the detected code problems and helps you quickly access the corresponding lines without scrolling the file. Hover over a mark on the stripe to see the detected problem in a tooltip. Click a mark to jump to the corresponding line.

### Navigate to detected problems

You can jump from one highlighted problem to another within a file by clicking ![the Next Highlighted Error button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.findAndShowNextMatches.svg) ![the Next Highlighted Error button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.findAndShowPrevMatches.svg) in the widget or by pressing `F2` or `Shift+F2` accordingly. By default, the IDE will navigate you to problems according to their [severity](configuring-inspection-severities.html): errors > warnings > weak warnings > server problems > typos.

You can configure IntelliJ IDEA to take you through the problems one by one regardless of their severity. Hover over the widget in top-right corner of the editor, click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg), select 'Next Error' Action (F2) Goes Through, and enable All Problems.

![Configuring navigation between highlighted lines](https://resources.jetbrains.com/help/img/idea/2025.3/navigate-inspection-lines.png)
