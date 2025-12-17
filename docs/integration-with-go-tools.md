[//]: # (Source: https://www.jetbrains.com/help/idea/integration-with-go-tools.html)
[//]: # (Downloaded: 2025-12-17 19:29:52)

## gofmt

IntelliJ IDEA includes built-in import management and a code formatter. Imports are handled on the fly. To customize how imports are processed, open settings by pressing `Ctrl+Alt+S` and navigate to Languages & Frameworks | Go | Imports. 

To reformat code, press `Ctrl+Alt+L`. Unlike `gofmt`, the IntelliJ IDEA formatter works with incomplete or syntactically incorrect code and can be applied to selected blocks. It also supports advanced formatting options such as inserting semicolons automatically, wrapping parameters, and more.

To run both formatters at once, enable the On Reformat Code action option under Editor | Code Style | Go on the Other tab.

You can also enable Reformat code in Actions on Save. This option is enabled by default. When you press `Ctrl+S`, the IDE runs both the built-in formatter and `gofmt`.

Use `gofmt` to format Go source code in the current file or across the whole project.

  * To format code in the currently opened file, navigate to Tools | Go Tools | Go Fmt File.

  * To format all code in the project, navigate to Tools | Go Tools | Go Fmt Project.

  * To format code before committing changes to VCS, select the Go fmt checkbox in the Commit dialog. For more information, refer to [Commit and push changes to Git repository](commit-and-push-changes.html).




To learn more, refer to [Command gofmt at pkg.go.dev](https://pkg.go.dev/cmd/gofmt).
