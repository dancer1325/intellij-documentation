[//]: # (Source: https://www.jetbrains.com/help/idea/dsm-analysis.html)
[//]: # (Downloaded: 2025-12-17 19:25:22)

## DSM tool window

View | Tool Windows | DSM

Note that the DSM tool window becomes available only after you have [built the matrix](#run-dsm).

Here you can see the typical matrix view.

![Matrix View](https://resources.jetbrains.com/help/img/idea/2025.3/dsmView.png)

The row headers represent the program structure. Everything is collapsed now, and only modules are shown. When expanded, the header is tree-like, allowing you to expand modules and dig into program packages. * — node groups classes inside the package. The column headers are the same as the corresponding row headers. Thus, they are not shown to save space. Instead, different visual aids are used on the row headers.

If you select a row, the matrix will look like this.

![Matrix view when a row is selected](https://resources.jetbrains.com/help/img/idea/2025.3/dsmView2.png)

Here you can learn the following:

  1. The selected row and corresponding column are highlighted to visualize row dependencies.

  2. The ellipsis in the cell means that the `maven-core` module has many (more than 99) dependencies on `maven-project` module.

  3. The column shows the dependencies of the selected row.

  4. The row shows the dependencies on the selected row.

  5. This means that the `maven-project` module has 16 dependencies on `maven-settings` module.

  6. Various shades correspond to the number of dependencies.


![Dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/dsmView3.png)

  * Color annotations help to visualize row dependencies at a glance.

  * `maven-core` depends on `maven-project`.

  * `maven-project` depends on `maven-profile`.

  * The dashes on the diagonal correspond to self-dependencies which are not shown.




You can select any cell to explore the dependencies indicated in it.

![Cell dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/dsmView4.png)

The cell #1 was selected. These color annotations mean that `maven-project` has 16 dependencies on`maven-settings`. The symmetrical cell (cell #2) shows dependencies in the other direction — in this case zero.

There is a simple mnemonic rule — all dependencies always _flow_ from Green to Yellow.

Instead of alphabetically sorting rows, DSM view sorts dependencies in a special way: classes, which are used most are moved to the bottom. In a project with good structure this creates a triangular shape in the lower left half of the matrix.

### Cycles

![Cycles](https://resources.jetbrains.com/help/img/idea/2025.3/dsmCycles.png)

Mutual dependencies are shown in red. It means that the plugin and usability packages are both dependent on each other.
