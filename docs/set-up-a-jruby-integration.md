[//]: # (Source: https://www.jetbrains.com/help/idea/set-up-a-jruby-integration.html)
[//]: # (Downloaded: 2025-12-17 20:00:18)

# Set up JRuby integration

JRuby allows you to seamlessly integrate Ruby code with the Java ecosystem by running Ruby on the Java Virtual Machine (JVM). By using JRuby, developers can access Java libraries from Ruby, execute Ruby scripts within Java projects, and build hybrid applications that leverage the strengths of both languages.

Before the integration, make sure that you have done the following:

  * [Installed and enabled the Ruby plugin](ruby-plugin.html#install_plugin_from_repo).

  * [Installed at least one JRuby interpreter](https://www.jruby.org/getting-started).




### Add JRuby support to your project

  1. In your project, go to File | Project Structure, or press `Ctrl+Alt+Shift+S`.

  2. Navigate to Facets and select JRuby from the dropdown. 

![Selecting the JRuby facet](https://resources.jetbrains.com/help/img/idea/2025.3/ij_jruby_facet_select.png)
  3. In the Choose Module dialog, select the module where you want to use JRuby and click OK. 

![Selecting a module for JRuby](https://resources.jetbrains.com/help/img/idea/2025.3/ij_jruby_to_module.png)
  4. After the JRuby facet is added, you can view it in the selected module. IntelliJ IDEA should detect all JRuby interpreters installed. In this case, make sure the required version is selected on the Gem Manager tab. For the selected Ruby interpreter/gemset, you can see the installed gems on the right.

![Gem Manager tab with a detected JRuby interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/ij_jruby_sdk_detected.png)

If there are no interpreters automatically detected, select one manually:

     1. Click the Add icon on the Gem Manager tab toolbar.

     2. Select Interpreter from the dropdown list. 

![Selecting the Interpreter option](https://resources.jetbrains.com/help/img/idea/2025.3/ij_interpreter_for_jruby.png)
     3. In the file browser window, navigate to the desired JRuby.exe file and select it.




26 June 2025

[Configure a Ruby interpreter](configuring-language-interpreter.html)[Rust](rust-plugin.html)
