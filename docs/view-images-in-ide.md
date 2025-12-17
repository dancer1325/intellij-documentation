[//]: # (Source: https://www.jetbrains.com/help/idea/view-images-in-ide.html)
[//]: # (Downloaded: 2025-12-17 20:06:14)

# Images

IntelliJ IDEA offers several ways to view images. You can use [navigation to source](#internal) or [open an image in an external graphical editor](#ext).

IntelliJ IDEA supports all popular image formats, such as PGN, JPG, and GIF. You can find a full list of supported file types in Settings (`Ctrl+Alt+S`): go to Editor | File Types and locate Image on the list. Learn more about file types in IntelliJ IDEA from [File type associations](creating-and-registering-file-types.html).

### View images in IntelliJ IDEA

  * In the Project tool window, find and select the image file.

Alternatively, place the caret at the reference to the image in the editor and press `Ctrl+B`.

  * To preview an image in a popup instead of in a separate tab, select the reference to it and press `Ctrl+Shift+I`.




### View images in an external editor

  * In the Project tool window, right-click the image file and select Jump to external editor.

Alternatively, press `Ctrl+Alt+F4`.

IntelliJ IDEA opens the image in the editor that is used in your OS by default. You can [configure another image editor](#change-external-editor) in which the IDE will open files.




### Change the default external editor

  1. Right-click an image in the editor and select Edit Path to External Editor from the context menu.

You can also press `Ctrl+Shift+A` and type `Edit Path to External Editor`.

  2. In the Path to External Editor dialog, specify the path to the application in which you want to open images and click Save. 

![Specifying the path to an external editor](https://resources.jetbrains.com/help/img/idea/2025.3/change-external-image-editor.png)



### Example: Import an image

Images belong to [resource files](resource-files.html). They should be stored in a dedicated folder – [Resources Root](content-roots.html#folder-categories). If you do not have this folder in your project, [create a new directory](add-items-to-project.html#new-directory), right-click it in the Project tool window, and select Mark Directory as | Resources Root.

  1. Copy the file in the file manager and then paste in to the folder with resource files in the IntelliJ IDEA Project tool window.

  2. In the dialog that opens, edit the filename and the target location if necessary. Click OK. 

![Importing an image](https://resources.jetbrains.com/help/img/idea/2025.3/image_in_resources_folder.png)
  3. Right-click the pasted image in the Project tool window and select Copy | Path From Source Root. 

  4. In the class in which you want to use the image, place the caret at the necessary line and press `Ctrl+V` to paste the path to the image. 

Run your application or a fragment of it to make sure that the image is inserted correctly.




18 September 2025

[Print files](print.html)[Scopes and file colors](configuring-scopes-and-file-colors.html)
