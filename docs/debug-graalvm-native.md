[//]: # (Source: https://www.jetbrains.com/help/idea/debug-graalvm-native.html)
[//]: # (Downloaded: 2025-12-17 19:24:15)

## Operating systems

GraalVM builds are not yet capable of producing [debug information](https://www.graalvm.org/latest/reference-manual/native-image/debugging-and-diagnostics/DebugInfo/) for operating systems other than Linux.

For debugging a native image on another operating system, you have to compile the executable for Linux and [run it in a Docker container](run-targets.html). If you're on Windows, you can also use [WSL](how-to-use-wsl-development-environment-in-product.html) for this purpose.

For requirements to the Docker container, refer to [Docker image](#docker_image).
