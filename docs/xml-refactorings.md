[//]: # (Source: https://www.jetbrains.com/help/idea/xml-refactorings.html)
[//]: # (Downloaded: 2025-12-17 20:07:42)

## Available XML refactorings

Delete attribute
    

The Delete Attribute refactoring allows you to delete a set of attribute definitions on a set of XML tag. If this refactoring is invoked, all attributes matching the selected attribute name on tags with the selected tag name may be removed.

Replace attribute with tag
    

The Replace Attribute with Tag refactoring allows you to replace attribute definitions on a set of XMLs tag with equivalent sub-tags. If this refactoring is invoked, all attributes matching the selected attribute name on tags with the selected tag name may be removed, and equivalent sub-tags created.

Replace tag with attribute
    

The Replace Tag with Attribute refactoring allows you to replace sub-tags definitions on a set of XMLs tag with equivalent attributes. If this refactoring is invoked, all tags matching the selected tag's name on tags with the selected parent tag name may be removed, and equivalent attributes created.

Add attribute
    

The Add Attribute refactoring allows you to add an attribute to a set of XML tags. If this refactoring is invoked, attributes matching the requested attribute name and value will be added to tags with the selected tag name. Optionally, the requested attribute may be added only to tags that do not already contain the selected attribute.

Add subtag
    

The Add Subtag refactoring allows you to add a subtag to a set of XML tags. If this refactoring is invoked, subtags matching with requested subtag name will be added to tags with the selected tag name. Optionally, the requested subtag may be added only to tags that do not already contain the selected subtag.

Move attribute in
    

The Move Attribute In refactoring allows you to move attributes defined on a set of XML tags inward to a set of subtags. If this refactoring is invoked, all attributes matching the selected attribute name on tags with the selected tag name may be moved inward toward a subtag of a given name.

Move attribute out
    

The Move Attribute Out refactoring allows you to move attributes defined on a set of XML tags outward to their parent tags. If this refactoring is invoked, all attributes matching the selected attribute name on tags with the selected tag name may be moved outward.

Change attribute value
    

The Change Attribute Value refactoring allows you to change the values an attribute defined on a set of XML tags. If this refactoring is invoked, all attributes matching the selected attribute name and selected attribute value on tags with the selected tag name may have their values changed.

Convert tag contents to attribute
    

The Convert Tag Contents to Attribute refactoring allows you to replace the contents of a set of XMLs tag with equivalent attributes. If this refactoring is invoked, all tags matching the selected tag's name will have their textual contents removed, and equivalent attributes created.

Delete tag
    

The Delete Tag refactoring allows you to delete a set of XML tags. If this refactoring is invoked, all tags matching the selected tag name on tags with the selected tag name may be removed.

Unwrap tag
    

The Unwrap Tag refactoring allows you to unwrap a set of XML tags, replacing them with their contents, if any. If this refactoring is invoked, all tags matching the selected tag name may be unwrapped. Note that top-level tags will not be unwrapped, as this may make XML documents invalid.

Wrap tag
    

The Wrap Tag refactoring allows you to wrap a set of XML tags in a newly created parent. If this refactoring is invoked, all tags matching the selected tag name may be wrapped.

Wrap tag contents
    

The Wrap Tag Contents refactoring allows you to wrap the contents of a set of XML tags in newly created tag. If this refactoring is invoked, all tags matching the selected tag name will have their contents wrapped.
