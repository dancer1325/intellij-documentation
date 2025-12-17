[//]: # (Source: https://www.jetbrains.com/help/idea/settings-smart-keys-php.html)
[//]: # (Downloaded: 2025-12-17 20:01:38)

# Smart Keys settings: PHP

Use this settings page to configure typing assistance features in PHP.

For more information about PHP support in IntelliJ IDEA, see [PHP](php-specific-guidelines.html).

Item| Description  
---|---  
Enable smart function parameters completion| When this checkbox is selected, you can use the “automatic” live template that provides completion lists for the parameters passed into functions, methods, or class constructors. To invoke the magic live template, type the params keyword as the first parameter in the call of the function, method, or class:![Smart parameters completion.png](https://resources.jetbrains.com/help/img/idea/2025.3/ps_smart_parameter_completion_step_1.png)IntelliJ IDEA displays a live template where the parameters are automatically completed with the variable names defined in the function declaration. To move to the next parameter, press `Enter` or `Tab`. To move to the previous parameter, press `Shift+Tab`.The completion list contains variables from a local scope in the next order: with the same type, with a similar name, defined nearby. You can always switch to the usual completion mode by pressing `Ctrl+Space` or just typing anything which is not in the list. Variables with similar names are inserted automatically.   
Select variable name without '$' sign on double click| When this checkbox is selected, only the variable name that follows the `$` sign is selected on double-click or pressing `Ctrl+W`. This is helpful if you often need to copy variable names without `$`: just double-click and copy the selection.If you still need a variable name with `$` selected, place the caret before the `$` sign and double-click it or press `Ctrl+W`.  
Remove PHP open/close tags while pasting in PHP context| If selected, IntelliJ IDEA automatically removes the opening and closing `<?php ?>` tags from the pasted Java code snippets.  
Escape symbols on paste in string literals| If selected, IntelliJ IDEA automatically inserts backslash escape symbols (`\`) when you paste text into a PHP string literal. For example, `'copied text'` becomes `\'copied text\'`.Clear the checkbox to suppress automatic symbols escaping.  
Replace unnecessary double quotes on paste| If selected, IntelliJ IDEA automatically replaces unnecessary double quotes with single quotes in pasted string literals. Such cases include the literals that do not contain string interpolation, escape sequences, or single quotes. For example, `echo "message"` becomes `echo 'message'`, while `echo "Error: $message"` remains intact.  
Auto-insert '<?php' tag after typing '<?'| If selected, IntelliJ IDEA automatically inserts the `<?php` opening tag when you type the `<?` short tag. Note that short tags are deprecated in PHP 7.4, and are planned for removal in PHP 8.0. For more information, refer to [RFC](https://wiki.php.net/rfc/deprecate_php_short_tags).  
Auto-insert semicolon when it is typed inside a function call| If selected, IntelliJ IDEA automatically moves the semicolon symbol `;` to the end of a function/method call when you type it after the last parameter inside the call. For example, `foo($a, $b;)` becomes `foo($a, $b);`  
Show additional options when searching for method usages| If selected, when you [search for usages](find-highlight-usages.html) of a method, IntelliJ IDEA will prompt you to choose whether you want to find usages of a base method or method's implementations.  
Auto-insert closing HTML tag in PHPDoc blocks| If selected, IntelliJ IDEA automatically adds closing HTML tags in [PHPDoc comments](https://www.jetbrains.com/help/phpstorm/phpdoc-comments.html) as you type.  
  
11 October 2024

[Smart Keys settings: JavaScript](settings-smart-keys-javascript.html)[Smart Keys settings: Python](settings-smart-keys-python.html)
