[//]: # (Source: https://www.jetbrains.com/help/idea/regex-search-and-replace-inspections.html)
[//]: # (Downloaded: 2025-12-17 19:57:04)

# Regex search and replace inspections

You can use regular expressions to create your own search and replace inspections. These inspections can be especially useful to highlight style-based or formatting-based problems.

### Access regex inspections

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections.

  2. From the options on the right, click ![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg).

  3. Select Add RegExp Search Inspection from the list, and you’ll be directed to a dialog where you can set up your new inspection.

![Add RegExp Search Inspection](https://resources.jetbrains.com/help/img/idea/2025.3/add_regex_inspection.png)
  4. Select the language, use hints on the left to build a regexp, and designate the required replacement for the selected pieces of code. You can also configure the way you want the IDE to highlight them in the project.

![Search RegExp](https://resources.jetbrains.com/help/img/idea/2025.3/search_regexp.png)
  5. In the editor, press `Alt+Enter` to invoke the inspection.

![Replace with regex result](https://resources.jetbrains.com/help/img/idea/2025.3/replace_with_regexp.png)



27 May 2025

[Regular expression syntax reference](regular-expressions.html)[Search for usages](find-highlight-usages.html)
