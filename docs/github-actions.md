[//]: # (Source: https://www.jetbrains.com/help/idea/github-actions.html)
[//]: # (Downloaded: 2025-12-17 19:28:05)

# GitHub Actions

GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that lets you automate your build, test, and deployment pipeline. IntelliJ IDEA recognizes GitHub YAML files and provides coding assistance for them. This includes workflow files stored in the .github/workflows directory of your repository and action files stored in the .github/actions directory. For more information, refer to the [GitHub Actions documentation](https://docs.github.com/en/actions).

### Enable the GitHub plugin

This functionality relies on the [GitHub](https://plugins.jetbrains.com/plugin/13115-github) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the GitHub plugin, and select the checkbox next to the plugin name.




IntelliJ IDEA supports the following features for working with GitHub files:

  * [Syntax highlighting](configuring-colors-and-fonts.html)

IntelliJ IDEA provides syntax highlighting for the YAML structure of files. You can customize the color scheme in Settings | Editor | Color Scheme | YAML.

  *   * [Inspections](https://www.jetbrains.com/help/inspectopedia/GitHub-actions.html)

You can detect cyclic job dependencies, invalid parameters or standard library function calls, undefined action or file references, undefined job dependencies, and undefined parameters in GitHub files.

![An inspection example: Undefined job dependency](https://resources.jetbrains.com/help/img/idea/2025.3/github-actions-inspection-example.png)

You can manage GitHub Actions inspections in the Settings dialog (`Ctrl+Alt+S`) under Editor | Inspections | GitHub actions.

  * [Code completion](auto-completing-code.html)

IntelliJ IDEA provides extensive completion support to help you write GitHub workflows and actions faster. This includes:

    * Completion for various GitHub Actions contexts, including `github.*`, `env.*`, `steps.*`, and `inputs.*`. This simplifies the process of scripting complex workflows and reduces the time spent searching for context-specific syntax and parameters.

    * Job dependency completion for `needs` and `runs-on` attributes.

    * YAML structure suggestions.

    * Action parameters, names, and version autocompletion for local actions and actions published in the `actions` organization on GitHub.

    * CRON expression support with validation and completion for scheduled workflows.

![CRON expression in a GitHub file](https://resources.jetbrains.com/help/img/idea/2025.3/cron-github-yaml.png)
    * Docker image and tag suggestions to integrate Docker containers into your actions.

    * JavaScript file path completion.

    * Branding support in action.yml, allowing you to specify icons and colors to visually distinguish your actions in GitHub Marketplace and workflows.

  * [Code navigation](navigating-through-the-source-code.html)

You can quickly navigate between declarations and usages of symbols in GitHub Actions files.

  * [Quick documentation](viewing-reference-information.html)

Hover over a symbol or use the Documentation tool window (`Ctrl+Q`) to view quick documentation.




### Create a new GitHub workflow

IntelliJ IDEA allows you to create YAML files for GitHub workflows only in the .github/workflows directory.

  1. In the Project tool window, right-click the .github/workflows directory and select New (or press `Alt+Insert`). Then, select the GitHub Workflow file type.

  2. In the New GitHub Workflow File dialog, specify the file name and press `Enter`.




### Create a new GitHub action

IntelliJ IDEA allows you to create YAML files for GitHub actions only in the .github/actions directory.

  1. In the Project tool window, right-click the .github/actions directory and select New (or press `Alt+Insert`). Then, select the GitHub Action file type.

  2. In the New GitHub Action File dialog, specify the file name and press `Enter`.




11 September 2025

[Share code with GitHub gists](share-code-with-gists.html)[GitLab](gitlab.html)
