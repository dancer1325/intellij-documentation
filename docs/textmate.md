[//]: # (Source: https://www.jetbrains.com/help/idea/textmate.html)
[//]: # (Downloaded: 2025-12-17 20:04:21)

## Import TextMate bundles

You can also download and use custom TextMate bundles for other languages. IntelliJ IDEA provides compatibility with several types of bundles, originally designed for different editors:

  * TextMate bundles are the original bundle types for TextMate editor. They are packaged in a directory with a  .tmBundle extension.

  * Sublime Text packages come with .tmLanguage and .tmPreferences files inside a directory. Since the original TextMate bundles also contain the same files, they are often used interchangeably.

  * Visual Studio Code extensions with a package.json file present in the directory.




Suppose you want IntelliJ IDEA to highlight syntax of the OCaml files.

  1. Download the [OCaml TextMate Bundle](https://github.com/textmate/ocaml.tmbundle). It is now on your disk.

  2. Press `Ctrl+Alt+S` to open settings and then select Editor | TextMate Bundles. 

  3. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and locate the OCaml bundle on your disk. It appears in the list of recognized bundles.



