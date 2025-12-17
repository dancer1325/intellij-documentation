[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-finding-and-replacing-text-using-regular-expressions.html)
[//]: # (Downloaded: 2025-12-17 20:04:44)

## Use regex capturing groups and backreferences

You can put the regular expressions inside brackets in order to group them. Each group has a number starting with 1, so you can refer to (backreference) them in your replace pattern. Note that the group 0 refers to the entire regular expression. However, you can refer to the captured group not only by a number `$n`, but also by a name `${name}`.

For example, for the numbered capturing groups, use the following syntax:

<h2>(.*?)</h2>

$1 

For the named capturing groups, use the following syntax:

<h2>(?<title>.*?)</h2>

${title} 

### Find and replace a captured group

Let's consider the following :

<new product="ij" category="105" title="Multiline search and replace in the current file"/> <new product="ij" category="105" title="Improved search and replace in the current file"/> <new product="ij" category="105" title="Regexp shows replacement preview"/>

  1. Open the search and replace pane `Ctrl+R`.

  2. In the search field, enter parentheses `()` that would indicate a [capturing group](https://www.regular-expressions.info/brackets.html), for example: `\stitle="(.*)?"\s*(/>*)`.

  3. In the replace field, [backreference](https://www.regular-expressions.info/backref.html) such groups by numbers starting with 1, for example: 

$2<title>$1</title>

.

  4. IntelliJ IDEA highlights the found occurrences based on your search specifications and displays hints with the replace string.

![Replace with regex result](https://resources.jetbrains.com/help/img/idea/2025.3/replace_with_regex.png)


