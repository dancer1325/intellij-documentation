[//]: # (Source: https://www.jetbrains.com/help/idea/resource-bundle.html)
[//]: # (Downloaded: 2025-12-17 19:57:43)

## Editing resource bundles

Once you create several [properties files](properties-files.html) with the same name and different locale suffixes, IntelliJ IDEA automatically recognizes them and groups them in the Project view into a resource bundle.

![Resource bundle](https://resources.jetbrains.com/help/img/idea/2025.3/resourceBundles.png)

The [Resource Bundle Editor plugin](internationalization-and-localization.html#install-plugin) provides an editor for convenient editing of localizable strings in properties files.

### Open the Resource Bundle editor

Do one of the following:

  * Select a resource bundle in the Project tool window, and press `F4`.

  * Open a properties file that is a part of a bundle and click the Resource Bundle tab at the bottom of the editor:

![Resource bundle editor tab](https://resources.jetbrains.com/help/img/idea/2025.3/bundleEditor1.png)



### Edit property keys

  1. Open a properties file.

  2. Add, change, or delete keys as required. IntelliJ IDEA reflects the changes in the Resource Bundle editor.




Use the Resource Bundle editor to change property values, which will ensure that you edit the entire set of property files simultaneously. IntelliJ IDEA creates respective records in each file of the bundle.

### Edit property values

  1. Select the property key in the left pane of the resource bundle editor.

  2. In the target locale frame, edit the value as required. IntelliJ IDEA updates the respective properties file accordingly.

![Resource bundle editor](https://resources.jetbrains.com/help/img/idea/2025.3/bundleEditor.png)



Here, you can also add new properties (use the ![the Property button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button), sort, and group properties.

When editing a resource bundle, keep the following in mind:

  * IntelliJ IDEA highlights properties with no values or those omitted in one of the properties files.

  * To convert between escape sequences (for example, `\u00df`) and unicode literals (corresponding national characters, such as `ß`) in properties files and in the Resource Bundle editor, select the Transparent native-to-ascii conversion checkbox on the [File Encoding](settings-file-encodings.html) page of the IDE settings.

For more information, refer to [Encoding](encoding.html).

  * It is possible to encode non-ASCII symbols using both uppercase and lowercase hex sequences (for example, `\u00E3` and `\u00e3`). By default, IntelliJ IDEA supports only uppercase sequences. To use lowercase hex sequences, set the `idea.native2ascii.lowercase` property in the idea.properties file to `true`.

For more information, refer to [Platform properties](tuning-the-ide.html#configure-platform-properties).



