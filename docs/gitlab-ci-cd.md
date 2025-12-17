[//]: # (Source: https://www.jetbrains.com/help/idea/gitlab-ci-cd.html)
[//]: # (Downloaded: 2025-12-17 19:28:08)

## Features

The following features are supported:

  * [Syntax highlighting](configuring-colors-and-fonts.html)

IntelliJ IDEA provides syntax highlighting for all components of GitLab CI/CD configuration files. You can customize the color scheme for different parts of the configuration:

    * YAML structure of your configuration file:

Settings | Editor | Color Scheme | YAML

    * [CI/CD variable expressions](https://docs.gitlab.com/ci/jobs/job_rules/#cicd-variable-expressions):

Settings | Editor |Color Scheme | GitLab CI Expression

    * [Shell script injections](#shell-injections):

Settings | Editor |Color Scheme | Shell Script

  * [Inspections](https://www.jetbrains.com/help/inspectopedia/GitLab-CI-CD.html)

IntelliJ IDEA helps you detect configuration issues in your GitLab CI/CD configuration file in real time. This includes duplicated job usage, undefined jobs, and undefined stages.

  * [Code completion](auto-completing-code.html)

Get completion suggestions for the pipeline configuration syntax, keywords, and CI/CD variables.

![Code completion for pipeline configuration syntax](https://resources.jetbrains.com/help/img/idea/2025.3/gitlab-ci-completion.png)
  * [Code navigation](navigating-through-the-source-code.html#go_to_declaration)

Quickly navigate between `stage` and `job` declarations and usages in your CI/CD configuration file.

  * [Quick documentation](viewing-reference-information.html)

Hover over a symbol or use the Documentation tool window (`Ctrl+Q`) to view quick documentation, including links to the official GitLab CI reference.

![Quick documentation for GitLab CI configuration](https://resources.jetbrains.com/help/img/idea/2025.3/gitlab-ci-quick-doc.png)
  * [Find usages](find-highlight-usages.html)

Search for usages of `stage` and `job` symbols directly in your configuration file.

  * [Rename refactoring](rename-refactorings.html)

You can change the name of `stage` and `job` symbols in declarations and usages by applying the Rename refactoring (`Shift+F6`).

  * Detection of Shell script language injections

IntelliJ IDEA automatically detects Shell script injections in `before_script`, `script`, and `after_script` blocks of your configuration file and marks them as Injected Language: Shell Script. The IDE treats these code snippets as full-featured Shell scripts. You can edit Shell script fragments, explain them, and benefit from language-specific features, like syntax highlighting and code completion.

You can disable this behavior using the Switch shell script injection intention action on the injected section in your configuration file. Note that switching Shell script injections on or off affects the whole project.

![Shell script injection in a GitLab CI configuration file](https://resources.jetbrains.com/help/img/idea/2025.3/shell-script-injection-gitlab-ci.png)


