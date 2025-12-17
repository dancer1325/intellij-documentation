[//]: # (Source: https://www.jetbrains.com/help/idea/integration-with-go-templates.html)
[//]: # (Downloaded: 2025-12-17 19:29:51)

# Go templates

Go has its own template engine that is split into two packages: text/template and html/template. These packages are similar in functionality, with the difference that html/template allows a user to generate HTML code that is safe against code injection, making it suitable for use on web pages and emails. Also, these packages provide coding assistance in other applications such as the configuration for [Helm](https://helm.sh/) and [the Kubernetes package manager](https://kubernetes.io/).

To specify mapping of a type between a Go template and an application, IntelliJ IDEA uses the `gotype` comment of the following structure: `{{- /*gotype: package/path.type_name*/ -}}`.

For Go templates, the commonly used file extensions are:

  * `.gohtml`: specifically indicates a Go HTML template, useful if your editor or IDE provides specialized support for these templates. IntelliJ IDEA has association with this extension.

  * `.tmpl`: a general extension for template files, suitable for Go templates.

  * `.tpl`: another general extension for template files used in Go.




### Define mapping of a type between Go template and application

  1. Add an HTML tag (for example, `<title></title>`).

  2. Inside an HTML tag, type `{{.}}`.

  3. Place the caret after the dot, press `Alt+Enter`, and select Specify dot type.

  4. In the `gotype` comment section, select the necessary type from the code completion popup `Ctrl+Space`.




[Files on GitHub](https://github.com/apronichev/documentation-code-examples/tree/master/goTemplates).

Alternatively, type `{{- /*gotype: */ -}}`, place the caret after `gotype:`, press `Ctrl+Space`, and select the necessary type.

11 October 2024

[Go workspaces](go-workspaces.html)[GOROOT and GOPATH](configuring-goroot-and-gopath.html)
