[//]: # (Source: https://www.jetbrains.com/help/idea/regular-expressions.html)
[//]: # (Downloaded: 2025-12-17 19:57:06)

## RegEx syntax reference

Character| Description  
---|---  
`\`| Marks the next character as either a special character or a literal. For example:

  * `n` matches the character `n`. `\n` matches a newline character.
  * The sequence `\\` matches `\` and `\(` matches `(`.

  
`^`| Matches the beginning of input.  
`$`| Matches the end of input.  
`*`| Matches the preceding character zero or more times. For example, `zo*` matches either `z` or `zoo`.  
`+`| Matches the preceding character one or more times. For example, `zo+` matches `zoo` but not `z`.  
`?`| Matches the preceding character zero or one time. For example, `a?ve?` matches the `ve` in `never`.  
`.`| Matches any single character except a newline character.  
`(` subexpression `)`| Matches _subexpression_ and remembers the match. If a part of a regular expression is enclosed in parentheses, that part of the regular expression is grouped together. Thus, a regex operator can be applied to the entire group.

  * If you need to use the matched substring within the same regular expression, you can retrieve it using the backreference `\num`, where `num = 1..n`.
  * If you need to refer the matched substring somewhere outside the current regular expression (for example, in another regular expression as a replacement string), you can retrieve it using the dollar sign `$num`, where `num = 1..n`.
  * If you need to include the parentheses characters into a _subexpression_ , use `\(` or `\)`.

  
`x|y`| Matches either `x` or `y`. For example, `z|wood` matches `z` or `wood`. `(z|w)oo` matches `zoo` or `wood`.  
`{n}`| `n` is a non-negative integer. Matches exactly `n` times. For example, `o{2}` does not match the `o` in `Bob`, but matches the first two o's in `foooood`.  
`{n,}`| `n` is a non-negative integer. Matches at least `n` times.For example, `o{2,}` does not match the _o_ in _Bob_ and matches all the o's in `food`.`o{1,}` is equivalent to `o+`. `o{0,}` is equivalent to `o*`.  
`{n,m}`| `m` and `n` are nonnegative integers. Matches at least _n_ and at most _m_ times. For example, `o{1,3}` matches the first three o's in `food`. `o{0,1}` is equivalent to `o?`.  
`[xyz]`| A character set. Matches any one of the enclosed characters. For example, `[abc]` matches `a` in `plain`.  
`[^xyz]`| A negative character set. Matches any character not enclosed. For example, `[^abc]` matches `p` in `plain`.  
`[a-z]`| A range of characters. Matches any character in the specified range. For example, `[a-z]` matches any lowercase alphabetic character in the range `a` through _z_.  
`[^m-z]`| A negative range of characters. Matches any character not in the specified range. For example, `[^m-z]` matches any character not in the range `m` through `z`.  
`\b`| Matches a word boundary, that is, the position between a word and a space. For example, `er\b` matches `er` in `never` but not the `er` in `verb`.  
`\B`| Matches a non-word boundary. `ea*r\B` matches the `ear` in `never early`.  
`\d`| Matches a digit character. Equivalent to `[0-9]`.  
`\D`| Matches a non-digit character. Equivalent to `[^0-9]`.  
`\f`| Matches a form-feed character.  
`\n`| Matches a newline character.  
`\r`| Matches a carriage return character.  
`\s`| Matches any whitespace including space, tab, form-feed, and so on. Equivalent to `[ \f\n\r\t\v]`.  
`\S`| Matches any nonwhite space character. Equivalent to `[^ \f\n\r\t\v]`.  
`\t`| Matches a tab character.  
`\v`| Matches a vertical tab character.  
`\w`| Matches any word character including underscore. Equivalent to `[A-Za-z0-9_]`. Use it in the search field.  
`\W`| Matches any non-word character. Equivalent to `[^A-Za-z0-9_]`.  
`\num`| Matches `num`, where `num` is a positive integer, denoting a reference back to remembered matches.For example, `(.)\1` matches two consecutive identical characters.  
`\n`| Matches `n`, where `n` is an octal escape value. Octal escape values should be 1, 2, or 3 digits-long. For example, `\11` and `\011` both match a tab character.`\0011` is the equivalent of `\001` & _1_.Octal escape values should not exceed 256. If they do, only the first two digits comprise the expression. Allows ASCII codes to be used in regular expressions.  
`\xn`| Matches `n`, where `n` is a hexadecimal escape value. Hexadecimal escape values must be exactly two digits long.For example, `\x41` matches `A`. `\x041` is equivalent to `\x04` & `1`.Allows ASCII codes to be used in regular expressions.  
`\$`| Finds a `$` character.  
`\\$`| This regex in the search field means that you are trying to find a `\` character at the end of the line.  
`\l`| Changes the case of the next character to the lower case. Use this type of regex in the replace field.  
`\u`| Changes the case of the next character to the upper case. Use this type of regex in the replace field.  
`\L`| Changes the case of all the subsequent characters up to `\E` to the lower case. Use this type of regex in the replace field.  
`\U`| Changes the case of all the subsequent characters up to `\E` to the upper case. Use this type of regex in the replace field.  
`(?!)`| This is a pattern for a negative lookahead. For example, `A(?!B)` means that IntelliJ IDEA will search for `A`, but only if not followed by `B`.  
`(?=)`| This is a pattern for a positive lookahead. For example, `A(?=B)` means that IntelliJ IDEA will search for `A`, but match if only followed by `B`.  
`(?<=)`| This is a pattern for a positive lookbehind. For example, `(?<=B)A` means that IntelliJ IDEA will search for `A`, but only if there is `B` before it.  
`(?<!)`| This is a pattern for a negative lookbehind. For example, `(?<!B)A` means that IntelliJ IDEA will search for `A`, but only if there is no `B` before it.  
  
Since IntelliJ IDEA supports all the standard regular expressions syntax, you can check <https://www.regular-expressions.info> for more information about the syntax.
