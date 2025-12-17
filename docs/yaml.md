[//]: # (Source: https://www.jetbrains.com/help/idea/yaml.html)
[//]: # (Downloaded: 2025-12-17 20:07:53)

## Anchors and aliases

IntelliJ IDEA supports working with anchors and aliases. If you specify a new anchor in the YAML file, the editor will show a warning that this anchor is not used by any node.

![YAML: unused anchor warning](https://resources.jetbrains.com/help/img/idea/2025.3/yaml_unused_anchor_warning.png)

The editor enables you now to [complete](auto-completing-code.html) aliases for this anchor.

![YAML: complete alias](https://resources.jetbrains.com/help/img/idea/2025.3/yaml_complete_alias.png)

You can [navigate](navigating-through-the-source-code.html) from aliases to the anchor using the `Ctrl+B` shortcut.

To quickly find usages of an anchor, place the caret on the anchor and press `Ctrl+B`.

![YAML: navigate to aliases](https://resources.jetbrains.com/help/img/idea/2025.3/yaml_navigate_aliases.png)

IntelliJ IDEA supports the [rename refactoring](rename-refactorings.html) for anchors and aliases: Place the caret on the anchor and press `Shift+F6`. Alternatively, right-click the anchor and select Refactor | Rename.

![renaming the YAML anchor](https://resources.jetbrains.com/help/img/idea/2025.3/yaml_rename_anchor.png)

Use the Structure tool window (`Alt+7`) to quickly navigate through YAML files. To show or hide elements of reused anchors in the Structure tool window, click ![View Options](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) use Aliased sub-trees.

![YAML structure view](https://resources.jetbrains.com/help/img/idea/2025.3/yaml_structure_view.png)
