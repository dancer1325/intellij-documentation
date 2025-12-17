[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-structure-of-a-source-file.html)
[//]: # (Downloaded: 2025-12-17 20:06:30)

## Structure popup

The popup provides less information than the [tool window](#structure-tool-window), but it allows you to navigate the structure faster due to the [Narrow down on typing](#narrow-down-typing) option.

  1. Open a file in the editor and press `Ctrl+F12`, or go to Navigate | File Structure in the main menu.

  2. In the popup, start typing the name of the element that you want to find. The IDE will narrow down the search results as you type.

You can also use CamelHumps, that is, for example, you can type `dsu` to match .

  3. You can additionally narrow down your search results by using the checkboxes in the popup. To change the sorting, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg) and select the necessary option. 

  4. Press `Enter` or click an item to close the popup and navigate to the selected element in the editor. 

![Structure popup](https://resources.jetbrains.com/help/img/idea/2025.3/file-structure-popup-menu.png)



Inherited members
    

Displays all methods and fields inherited by the current class and accessible from it. The inherited members are displayed gray to distinguish them from the members defined in the current class. 

Anonymous Classes
    

Displays inner anonymous classes in the tree view.

Lambdas
    

Displays all lambdas in the tree.

Alphabetically
    

Sorts elements within a class alphabetically.

By Visibility
    

Sorts items by their visibility in the following order: public - protected - package local - private.

Narrow down on typing
    

Hides irrelevant items [as you type](speed-search-in-the-tool-windows.html). When this option is disabled, the IDE highlights all items that match your search query without hiding irrelevant items.
