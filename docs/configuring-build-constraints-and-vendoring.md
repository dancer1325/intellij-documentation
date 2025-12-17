[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-build-constraints-and-vendoring.html)
[//]: # (Downloaded: 2025-12-17 19:21:41)

## Build constraints

A build constraint, also known as a build tag, is a line comment that outlines the conditions under which a file is included in the package. These tags can specify requirements such as the operating system, architecture, Go version, compiler, cgo support, or other target system needs. In the example below, we declare that this file is for the target system meeting the following criteria:

  * `//+build darwin,cgo linux` is the older syntax for build tags, still recognized in Go. It specifies two sets of conditions:

    * `darwin,cgo`: Include in the build when compiling for the `darwin` platform (macOS) and when `cgo` is enabled. `cgo` enables the inclusion of C code in Go programs.

    * `linux`: Include when compiling for the Linux platform.

The space acts as an OR operator, meaning the file should be included for macOS with cgo enabled or for Linux.

  * `//go:build (darwin && cgo) || linux` is the newer syntax for build tags, introduced in Go 1.17, using a more explicit boolean expression format:

    * `(darwin && cgo) || linux`: The file should be included in the build for macOS with cgo enabled or for Linux, identical to the above condition.


![Build constraints](https://resources.jetbrains.com/help/img/idea/2025.3/go_example_build_constraints.png)

IntelliJ IDEA can use these constraints to decide what files must be ignored during validation, resolving, and symbol suggestions. If the file does not satisfy the requirements of the target system, IntelliJ IDEA displays a notification. For example, the following conditions on the screenshot will conflict with settings from [the Configure build constraints for your project procedure](#configure-build-constraints-for-your-project).

![Notification about build constraints](https://resources.jetbrains.com/help/img/idea/2025.3/go_example_build_constraints_invalid.png)

### Configure build constraints for your project

The `go build` command in Go [supports](https://pkg.go.dev/cmd/go) the use of custom tags through the `-tags` argument to conditionally compile files based on build constraints. These tags allow you to specify conditions under which files are included in the build process.

In your Go source files, you can define build constraints by placing a comment at the top of the file that includes the `// +build` or `//go:build` directive followed by the custom tags.

  1. Open settings (`Ctrl+Alt+S`) and navigate to Languages & Frameworks | Go Build tags.

  2. From drop-down lists, select expected values for the target system. If you have any custom tags, specify them in the Custom tags field (use a space between tags as a separator).

  3. Click OK.

![Configure build constraints for your project](https://resources.jetbrains.com/help/img/idea/2025.3/go_configure_project_build_contraints.png)



### Using Go experiments

  1. Open settings by pressing `Ctrl+Alt+S` and navigate to Go | Build Tags.

  2. Type tags for Go Experiments in one of the fields:

     * Custom tags: type tags in the following format: `goexperiment.rangefunc goexperiment.loopvar`. Use spaces to separate tags from each other.

     * Experiments: type tags in the following format: `rangefunc, loopvar`. Use commas to separate tags from each other.

Tag names are located within the corresponding packages. For instance, upon accessing the `iter` package, you will notice the tag name directly following the `go:build` tag. Specifically for the `iter` package, the tag is `goexperiment.rangefunc`. In the Custom tags field, enter the complete tag, whereas in the Experiments field, input only the segment subsequent to `goexperiment.`.




### Description of Build Tags fields

For more information about build tags or constraints, see [Build constraints at pkg.go.dev](https://pkg.go.dev/cmd/go#hdr-Build_constraints).

Field| Build Tags| Description  
---|---|---  
Operating System| `GOOS`| Specifies the operating system you're compiling your code for, such as `linux` or `windows`.  
Architecture| `GOARCH`| Defines the CPU architecture for your code, like `amd64` or `arm`.  
Go Version| `GOVERSION`| Tells you the Go version installed. It is the same version you see when you run `go version`.  
Compiler| | Chooses the compiler, like `gccgo` or `gc`, based on what is available in your runtime.  
CGO Support| `CGO_ENABLED`| Shows if cgo is enabled (1) or disabled (0), affecting whether you can include C code.  
Custom Tags| | Any build tags introduced by the `//go:build` comment line.For example, in the following screenshot, the `goexperiment.rangefunc` build tag enables iteration over a function from [Go Experiments](https://pkg.go.dev/internal/goexperiment).  
Experiments| `GOEXPERIMENT`| A list of Go toolchain experiments you can turn on or off. Mainly for developers working on Go itself.  
  
### Using multiple conditions for build constraints

Due to the introduction of a new syntax for build constraints, consider the following table that lists the differences between two syntaxes when using multiple conditions.

`//+build`| `//go:build`  
---|---  
//+build darwin,cgo linuxA comma (as a logical And) and a whitespace (as a logical Or)| //go:build (darwin && cgo) || linuxThe `&&` operator (logical `And`) and the `||` operator (logical `Or`)
