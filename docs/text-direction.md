[//]: # (Source: https://www.jetbrains.com/help/idea/text-direction.html)
[//]: # (Downloaded: 2025-12-17 20:04:19)

# Text direction

IntelliJ IDEA enables you to choose the base direction for rendering strings and tokens (for example, in [properties files](properties-files.html)) , containing bidirectional text, like a mix of English and Hebrew or Arabic.

By default, the direction for rendering is content-based, which means that text direction is defined by the text with which the string begins. For example, if the string starts with English, then the base direction of the text is considered left-to-right.

However, it is also possible to always use either left-to-right or right-to-left as the base direction.

### Choose the direction for rendering bidirectional strings

  * When you open a file with bidirectional strings in the editor, a notification panel appears allowing you to change the direction. Click Choose direction on the panel.

![Choosing direction for rendering bidirectional strings](https://resources.jetbrains.com/help/img/idea/2025.3/bidi-text-properties.png)
  * Go to View, point to BiDi Text Base Direction, and select the required direction.




Depending on the selection, bidirectional string literals change their appearance:

![Bidirectional strings](https://resources.jetbrains.com/help/img/idea/2025.3/bidi_text_results.png)

07 October 2025

[Hard-coded string literals](hard-coded-string-literals.html)[Vim in IntelliJ IDEA](using-product-as-the-vim-editor.html)
