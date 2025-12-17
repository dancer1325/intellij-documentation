[//]: # (Source: https://www.jetbrains.com/help/idea/using-postfix-templates.html)
[//]: # (Downloaded: 2025-12-17 20:05:39)

# JavaScript postfix templates

Learn more from [Postfix Code Completion](http://blog.jetbrains.com/idea/2014/03/postfix-completion/#sthash.mI1AHa17.dpuf).

Postfix code completion lets you add template code around an expression you’ve just typed. A template expands when you type its abbreviation (postfix) after a dot and press the expansion key (`Tab` by default) or when you select the abbreviation in the code completion popup. For example, the `.if` postfix applied to an expression wraps it with an `if` statement. 

IntelliJ IDEA is shipped with a set of predefined postfix templates and lets you define your own custom ones, refer to [Create custom postfix templates](postfix-code-completion.html#custom-postfix-templates). 

Custom templates can be copied, updated, and removed. For predefined templates you can only change their postfixes, for example, to replace a long key with a shorter one.

Before| After  
---|---  
function m(arg) { arg.if } |  function m(arg) { if (arg) { } }   
  
Learn more from [Postfix code completion](postfix-code-completion.html) and [IntelliJ IDEA blog](http://blog.jetbrains.com/idea/2014/03/postfix-completion/#sthash.mI1AHa17.dpuf). .

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | General | Postfix Completion.

  2. On the Postfix Completion page, that opens, select the Enable postfix templates checkbox.

The page shows a list of available postfixes with the corresponding templates next to them. When you select a postfix, the Description pane illustrates the corresponding transformation showing the code snippet before and after the template is expanded.

To activate a postfix, select the checkbox next to it.




### Apply a postfix template

  1. Type your expression followed by a dot.

  2. Type the postfix and press the expansion key (by default `Tab`) or select the postfix from the suggestion list. If necessary, choose an expression to be surrounded or replaced.

The default expansion key for all postfix templates is `Tab`. See [Changing the default expansion key](#postfix_completion_change_default_expansion_key) to learn how to choose another one.




### Create a custom template

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | General | Postfix Completion.

  2. On the Postfix Completion page that opens, click ![Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose the language where the template will work. You can choose JavaScript and TypeScript or TypeScript.

  3. In the Create new template dialog that opens:

     * Specify the template postfix in the Key field.

     * Select the language level from the Minimum language level list.

     * Type the template code, adding `$EXPR$` in the places where you need to insert the initial expression. Add `$END$` where you want the caret to be at the end.

![Postfix completion: create custom template](https://resources.jetbrains.com/help/img/idea/2025.3/ws_postfix_completion_settings_page_create_template_dialog.png)



You can also create a new template that slightly differs from an existing one, for example, in its language context or the final position of the caret. IntelliJ IDEA lets you copy the original template and make the necessary changes in that copy.

### Create a new custom template from an existing one

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | General | Postfix Completion.

  2. On the Postfix Completion page that opens, select the custom template from which you want to create a new one and click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg) on the toolbar.

  3. In the Edit template dialog that opens, edit the template as necessary and type a new postfix.




### Change the default expansion key

  * In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | General | Postfix Completion, and choose a new key from the Expand templates with list.




### Disable postfix completion

  * To suppress expanding all the configured postfix templates, clear the Enable postfix templates checkbox.

  * To suppress expanding a specific template, clear the checkbox next to its postfix.




10 March 2025

[JavaScript documentation look-up](viewing-javascript-reference.html)[JavaScript linters](linters.html)
