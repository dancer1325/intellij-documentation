[//]: # (Source: https://www.jetbrains.com/help/idea/go-plugin-test-configurations.html)
[//]: # (Downloaded: 2025-12-17 19:28:15)

## Packages for testing

For testing purposes, IntelliJ IDEA includes the following packages:

gotest
    

Use for running standard unit tests. For more information about `go test`, refer to [Package testing](https://pkg.go.dev/testing).

gocheck
    

Use to have extended functionality of `go check` and running more complex tests. For more information about `go check`, refer to [go check](https://pkg.go.dev/gopkg.in/check.v1).

gobench
    

Use for running performance tests. For more information about `gobench`, refer to [Package testing: Benchmarks](https://pkg.go.dev/testing#hdr-Benchmarks).

go test -fuzz
    

Use for running fuzzing tests. Fuzzing in Go is a technique used to automatically test software by providing it with a large amount of random or unexpected input to uncover vulnerabilities or bugs. For more information about `go test -fuzz`, refer to [Go Fuzzing](https://go.dev/security/fuzz/).

![Packages for testing](https://resources.jetbrains.com/help/img/idea/2025.3/go_ij_testing_packages.png)
