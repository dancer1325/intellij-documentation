[//]: # (Source: https://www.jetbrains.com/help/idea/shebang-scripts.html)
[//]: # (Downloaded: 2025-12-17 20:02:40)

# Run shebang scripts

Starting with version 11, Java provides a way to run self-contained scripts without the need to compile them (<https://openjdk.java.net/jeps/330>). Furthermore, on Linux and macOS, you can create scripts in Java by specifying the JDK in the first line of the file.

This is called [the shebang mechanism](https://en.wikipedia.org/wiki/Shebang_\(Unix\)). Shebang support in Java comes in handy when you need to write an executable script, but you don't want to install a compiler or use a scripting language like bash.

### Write a script

  1. Create a file without the `.java` extension.

  2. Start the first line with `#!` followed by the path to the JDK that will be used to run the script. Use `source` to specify the language level of the script. Language level 11+ is required.

Example:

`#!/usr/lib/jvm/openjdk-14.0.1/bin/java --source 11`

  3. Write the body of the script. The script can contain multiple classes and use imports from the standard library. The entry point has to be defined as `public static void main(String[] args)` in the first declared class.

Below is an example of a valid shebang script:

#!/usr/lib/jvm/openjdk-14.0.1/bin/java --source 11 import java.util.Locale; class Hello { public static void main(String[] args) { String lang = Locale.getDefault().getLanguage(); System.out.println(Greetings.getGreeting(lang)); } } class Greetings { static String getGreeting(String lang) { switch (lang) { case "fr": return "Bonjour"; case "es": return "Hola"; case "zh": return "Nǐn hǎo"; case "de": return "Guten Tag"; case "pl": return "Dzień dobry"; case "el": return "Yassas"; case "sv": return "God dag"; default: return "Hi"; } } } 

  4. Make sure that the script file is executable using the `chmod +x` command.




### Run a script

  * Click the Run icon in the gutter or press `Ctrl+Shift+F10`.

![Run button in the editor gutter](https://resources.jetbrains.com/help/img/idea/2025.3/shebang_run.png)
  * [Create](shell-scripts.html#run-shell-scripts) a run/debug configuration. This can be useful if you want to pass parameters to your script, debug it, or run it as part of a [compound workflow](run-debug-multiple.html#compound-configs).




### Debug a script

  1. [Create](shell-scripts.html#run-shell-scripts) a run/debug configuration for the script and [add a VM option to load the debug agent](attach-to-process.html#debug-agent).

  2. [Attach to the process](attach-to-process.html) using the Remote JVM debug run/debug configuration.




11 November 2024

[Run anything](running-anything.html)[Run targets](run-targets.html)
