[//]: # (Source: https://www.jetbrains.com/help/idea/settings-emmet.html)
[//]: # (Downloaded: 2025-12-17 20:01:03)

## Emmet.HTML

Item| Description  
---|---  
Enable XML/HTML Emmet| Select this checkbox to enable Emmet support for XML and HTML. If this checkbox is not selected, complicated abbreviations, such as `div.class>ul#list>.item$)` and similar, will not work in the editor.  
Enable abbreviation preview| Select this checkbox to have IntelliJ IDEA show a popup with a preview of the entered abbreviation before actually expanding it. ![Abbreviation preview](https://resources.jetbrains.com/help/img/idea/2025.3/emmet_abbreviation_preview.png)  
Enable automatic URL recognition while wrapping text with <a> tag| 

  * If this checkbox is cleared, and you wrap (`Ctrl+Alt+J`) a URL address with the `<a>` tag, IntelliJ IDEA encloses the URL address in `<a href=""></a>` and places the caret inside the double quotes in the `href` attribute. For example, wrapping `https://www.jetbrains.com` will result in the following: `<a href="`|`">https://www.jetbrains.com</a>`
  * If this checkbox is selected, and you wrap (`Ctrl+Alt+J`) a URL address with the `<a>` tag, IntelliJ IDEA inserts the URL address inside the double quotes as the value of the `href` attribute and encloses the URL in `<a href="<wrapped URL>"></a>`. For example, wrapping `https://www.jetbrains.com` will result in the following: `<a href="https://www.jetbrains.com">https://www.jetbrains.com</a>`

  
Add edit point at the end of template| 

  * If this checkbox is selected, an editing position adds to the end of an HTML template ($END$).
  * if this checkbox is not selected, then the new edit point is not added.Compare the following:![Edit point at the end of template](https://resources.jetbrains.com/help/img/idea/2025.3/emmet_cursor_position.png)

  
BEM| In this area, specify the BEM separators for the class names, modifiers and short elements. For more information, refer to the [Emmet documentation](https://docs.emmet.io/filters/bem/).  
Filters enabled by default| In this area, specify which Emmet filters you want to be applied to an expanded abbreviation before it is shown in the editor. Learn more about filters at <https://docs.emmet.io/filters/>. To have a filter always applied by default, select the checkbox next to it. The available options are:

  * [XSL tuning](https://docs.emmet.io/filters/#xsl-tuning-xsl)
  * [Comment tags](https://docs.emmet.io/filters/#comment-tags-c)
  * [Escape](https://docs.emmet.io/filters/#escape-e)
  * [Single line](https://docs.emmet.io/filters/#single-line-s)
  * [BEM](https://docs.emmet.io/filters/bem/)
  * [Trim line markers](https://docs.emmet.io/filters/#trim-line-markers-t)


