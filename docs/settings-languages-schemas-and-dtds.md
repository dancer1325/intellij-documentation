[//]: # (Source: https://www.jetbrains.com/help/idea/settings-languages-schemas-and-dtds.html)
[//]: # (Downloaded: 2025-12-17 20:01:16)

## External Schemas and DTDs

Local XML schema (XSD) and DTD files that are used to validate your XML files are listed in this section.

Each entry is a mapping of a URI that may be referenced in your XML file onto an appropriate local schema or DTD file. Use ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), ![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) and ![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) to create, remove and edit the mappings. See also, [Referencing XML schemas and DTDs](referencing-xml-schemas-and-dtds.html).

Item| Keyboard Shortcut| Description  
---|---|---  
URI| | A URL of an XML schema (XSD) or DTD file (for example http://www.example.org/xsds/example.xsd) or a namespace URI (for example http://www.example.org, urn:jboss:domain:1.0). Readonly.If an XML file references the specified URI, it's validated according to a local file whose path is shown in the Location columns.  
Location| | Path to corresponding local XSD or DTD file (readonly).  
Project| | If a checkbox is not selected, a mapping is available in all of your projects. Select the mappings that you want to be available only in the current project.The selected mappings are stored in .idea/misc.xml or the project .ipr file. These files are normally shared between development team members through version control.  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Use this icon or shortcut to open the Map External Resource Dialog to define a new mapping between a URI and a local file.  
![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Use this icon or shortcut to remove the selected mappings from the list.  
![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| `Enter`| Use this icon or shortcut to edit the selected mapping in the Map External Resource Dialog.
