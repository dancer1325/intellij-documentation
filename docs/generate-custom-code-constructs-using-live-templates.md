[//]: # (Source: https://www.jetbrains.com/help/idea/generate-custom-code-constructs-using-live-templates.html)
[//]: # (Downloaded: 2025-12-17 19:27:24)

# Generate custom code constructs using live templates

IntelliJ IDEA provides a multitude of predefined [live templates](using-live-templates.html) for many common code constructs. You can also define custom templates to cover use cases specific to your workflow.

### Insert a live template

  1. Place the caret at the place where you want the template to expand.

  2. Type the template abbreviation and press the invocation key (usually `Tab` by default). Alternatively, on the Code menu, click Insert Live Template `Ctrl+J` to open the [suggestion list](auto-completing-code.html#completion_tips) and select the necessary template.

  3. If the selected template requires user input, the corresponding field is highlighted. Type the necessary value and press `Enter` or `Tab` to complete input and move to the next input field. After completing all input fields, the caret moves to the end of the construct (or to the `$END$` marker if the marker is defined in the template code), and the editor returns to the regular mode of operation.




You can also wrap fragments of code using [surround templates](using-live-templates.html).

### Surround a block of code with a live template

  1. Select a piece of code to be surrounded.

  2. On the Code menu, click Surround With `Ctrl+Alt+J` to open the [suggestion list](auto-completing-code.html#completion_tips) and select the necessary template.




08 October 2024

[toString() Generation Settings dialog](generate-tostring-settings-dialog.html)[Implement methods of an interface or abstract class](implementing-methods-of-an-interface.html)
