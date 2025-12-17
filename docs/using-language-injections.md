[//]: # (Source: https://www.jetbrains.com/help/idea/using-language-injections.html)
[//]: # (Downloaded: 2025-12-17 20:05:29)

## Add language injections

### Add a temporary language injection

  1. Place the caret inside the string literal, tag, or attribute, in which you want to inject a language and press `Alt+Enter` (or use the intention action icon ![intention action icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.codeInsight.intentionBulb.svg)).

  2. Select Inject language or reference and choose the language you want to inject.




If the Inject language or reference intention action is not available by default, go to Settings (`Ctrl+Alt+S`) | Editor | Intentions and select the Inject language or reference checkbox in the Language injection section.

![Inject language or reference checkbox](https://resources.jetbrains.com/help/img/idea/2025.3/inject_language_or_reference.png)

### Add a persistent language injection

Use language injection comments (annotations) to add persistent fragments of injected languages.

  * Add a blank line before the target string literal, and type the following comment:

// language=<language_ID>

![Use language injection comments](https://resources.jetbrains.com/help/img/idea/2025.3/injection-comment.png)

For comments, use the syntax of the language you want to inject. Language IDs are generally intuitive, for example, SQL, RegExp, XML, HTML.

You can also learn language IDs in settings. Press `Ctrl+Alt+S` to open settings and then select Editor | language Injections. Double-click an injection rule for a language; the language ID is specified in the ID field.

  * (Optional) Include a prefix or a suffix in your comment. 

// language=<language_ID> prefix=<prefix> suffix=<suffix>

This is required if:

    * The string is an incomplete/partial SQL statement

    * The string is not used directly in one of our supported calls (such as `select /where)`



