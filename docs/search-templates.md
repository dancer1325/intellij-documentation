[//]: # (Source: https://www.jetbrains.com/help/idea/search-templates.html)
[//]: # (Downloaded: 2025-12-17 20:00:00)

## Count modifier

The Count modifier specifies a number of occurrences.

For example, in the `new java.lang.RuntimeException($x$)` search template, for `$x$` variable specify min and max numbers in the Count modifier field. To set the unlimited maximum count, provide an empty value in the modifier field.

![Count modifier](https://resources.jetbrains.com/help/img/idea/2025.3/ssr_count_filter.png)

IntelliJ IDEA adds `[0,∞]` to the variable and searches for the specified range of numbers.
