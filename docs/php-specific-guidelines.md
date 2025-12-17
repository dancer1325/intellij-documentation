[//]: # (Source: https://www.jetbrains.com/help/idea/php-specific-guidelines.html)
[//]: # (Downloaded: 2025-12-17 19:33:54)

## Work with PHP projects in IntelliJ IDEA

### Configure PHP environment

The PHP development environment includes a PHP engine, a web server, and a database server—the so-called AMP (Apache, MySQL, PHP) technology stack that can be installed as a preconfigured package (like [XAMPP](https://www.apachefriends.org/download.html) or [MAMP](https://www.mamp.info/en/downloads/)) or separate components to the local or remote operating system, in a virtual machine, or in a Docker container.

IntelliJ IDEA integrates with your PHP development environment for running, debugging, or unit testing the applications opened in the IDE.

To integrate your development environment with IntelliJ IDEA:

  1. Integrate your PHP engine with IntelliJ IDEA as described in [Configure local PHP interpreters](https://www.jetbrains.com/help/phpstorm/configuring-local-interpreter.html) or [Configure remote PHP interpreters](https://www.jetbrains.com/help/phpstorm/configuring-remote-interpreters.html).

  2. Set connection between IntelliJ IDEA and your web server as described in [Connect to a web server](configuring-synchronization-with-a-remote-host.html).

  3. Integrate your database server with IntelliJ IDEA as described in [Create a data source](managing-data-sources.html#create_a_data_source).

  4. Set up a debugging engine as described in [Debugging: Ultimate Guide](https://www.jetbrains.com/help/phpstorm/debugging-with-phpstorm-ultimate-guide.html).




### Open or create a PHP project

You can [open](import-project-or-module-wizard.html) or clone an existing PHP project in IntelliJ IDEA or create a new one. To create a PHP project:

  1. Go to File | New | Project or on the Welcome screen, click New Project.

  2. In the New Project dialog that opens:

     * Provide the name of the new project folder and the path to it.

To run and debug your application on a local Web server, create the project root below the Web server document root. Thus, your application sources will be "visible" for the local Web server.

     * Select PHP as the project type.

     * Select the Add 'composer.json' checkbox to automatically create a `composer.json` file for project dependencies. 

For more information about Composer support in the PHP plugin, see [Composer dependency manager](https://www.jetbrains.com/help/phpstorm/using-the-composer-dependency-manager.html).

![New PHP project](https://resources.jetbrains.com/help/img/idea/2025.3/ij_create_new_php_project.png)



### Code with smart assistance

  * PHP code completion. The PHP plugin helps you speed up the coding process with context-aware [PHP code completion](https://www.jetbrains.com/help/phpstorm/auto-completing-code.html) and [PHP type checking](https://www.jetbrains.com/help/phpstorm/php-type-checking.html).

![Array shape example](https://resources.jetbrains.com/help/img/idea/2025.3/ps_array_shape_completion.png)
  * Static code analysis. The PHP plugin comes with an extensive set of [inspections](running-inspections.html) for static analysis of PHP code. A specific type of inspections is [code quality checks by third-party tools](https://www.jetbrains.com/help/phpstorm/php-code-quality-tools.html), such as PHP CS Fixer, Laravel Pint, PHPStan, Psalm, PHP_CodeSniffer, and PHP Mess Detector.

![View insceptions in the editor](https://resources.jetbrains.com/help/img/idea/2025.3/php_inspections_in_opened_file_ij.png)

Inspections not only tell you where a problem is, but also provide [quick-fixes](resolving-problems.html) that help you deal with it right away. For the code that is correct (that is, not highlighted in the editor) but can still be optimized in the current context, there are [intention actions](intention-actions.html).

  * Code generation and live templates. The plugin provides multiple ways to [generate](generating-code.html) boilerplate PHP code. For bigger code constructs, such as loops, conditions, declarations, or print statements, there are [PHP live templates](https://www.jetbrains.com/help/phpstorm/using-live-templates.html).

![ps_quick_start_generate_code_mac.png](https://resources.jetbrains.com/help/img/idea/2025.3/ps_quick_start_generate_code_mac.png)
  * PHPDoc comments. For documentation comments, the plugin provides completion that is enabled by default. IntelliJ IDEA creates stubs of [PHPDoc blocks](https://docs.phpdoc.org/guide/getting-started/what-is-a-docblock.html) when you type the `/**` opening tag and press `Enter`, or press `Alt+Insert` and appoint the code construct (a class, a method, a function, and so on) to document. 

![Generate PHPDoc](https://resources.jetbrains.com/help/img/idea/2025.3/ps_reference_generate_phpdoc.png)

For more information, see [PHPDoc comments in PhpStorm](https://www.jetbrains.com/help/phpstorm/phpdoc-comments.html).




### Run PHP code

There are several ways to [run](running-applications.html) a PHP application in IntelliJ IDEA:

  * From IntelliJ IDEA using a [run configuration](run-debug-configuration.html) of the type [PHP Web Page](https://www.jetbrains.com/help/phpstorm/run-debug-configuration-php-web-application.html) to view application output in a browser.

  * From IntelliJ IDEA using a [PHP Script](https://www.jetbrains.com/help/phpstorm/run-debug-configuration-php-script.html) run configuration to view the application output in the Run tool window.

  * From IntelliJ IDEA, using a [built-in Web server](https://www.jetbrains.com/help/phpstorm/run-debug-configuration-php-built-in-web-server.htmlComposer_Page.topic). This approach saves your time and effort because you do not need to deploy the application sources.





### Debug PHP code

The plugin supports PHP code debugging with Xdebug and Zend Debugger. With Xdebug, the IDE automates the process of getting the debugger up and running, showing you the necessary prompts and action links as you go.

For the detailed guide and troubleshooting instructions, refer to [Debugging: Ultimate Guide](https://www.jetbrains.com/help/phpstorm/debugging-with-phpstorm-ultimate-guide.html) in PhpStorm documentation.

Besides interactive debugging, the IDE's integration with [Xdebug](http://xdebug.org/) also supports profiling. IntelliJ IDEA provides visual representation of the profiling snapshots generated by Xdebug to help you examine how your PHP application uses execution time and memory.

For more information, refere to [Profiling with Xdebug](https://www.jetbrains.com/help/phpstorm/profiling-with-xdebug.html) in PhpStorm documentation.




### Test PHP code

The PHP plugin supports integration with the most popular PHP test frameworks: [PHPUnit](https://www.jetbrains.com/help/phpstorm/using-phpunit-framework.html), [Pest](https://www.jetbrains.com/help/phpstorm/pest.html), [Behat](https://www.jetbrains.com/help/phpstorm/using-behat-framework.html), [PHPSpec](https://www.jetbrains.com/help/phpstorm/using-phpspec.html), and [Codeception](https://www.jetbrains.com/help/phpstorm/using-codeception-framework.html), so that you could create, manage, execute tests and review test results from within the IDE.

You can configure and run tests in different modules of a PHP project independently of one another. If your PHP project contains multiple [Composer-managed subprojects](https://www.jetbrains.com/help/phpstorm/using-the-composer-dependency-manager.html#manage-multiple-composer-files), and each of such subprojects has its own test framework executable and/or configuration file, IntelliJ IDEA creates a separate test framework configuration for each subproject.

For more information, refer to [Testing](https://www.jetbrains.com/help/phpstorm/testing.html) in PhpStorm documentation.




### Deploy PHP application

With IntelliJ IDEA, you can flexibly configure deployment of PHP applications. For example, you can set up your PHP project on a local Web server from the very beginning, or develop and test an application locally and then upload it to a remote Web server, and so on.

For more information, refer to [Deploy your application](https://www.jetbrains.com/help/phpstorm/deploying-applications.html) in PhpStorm documentation.



