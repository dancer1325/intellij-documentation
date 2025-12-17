[//]: # (Source: https://www.jetbrains.com/help/idea/prerequisites.html)
[//]: # (Downloaded: 2025-12-17 19:34:12)

## Minimal requirements

  * 4 vCPUs, either `x86_64` or `arm64` architecture. Also, higher clock frequency is preferred to higher core count.

  * 8 GB RAM.

  * Around 10 GB of free space is required on a local disk or on a network block storage, such as EBS.

A network file system such as NFS or SMB is not acceptable.

  * A supported version of a common Linux distribution.

Specifically, Ubuntu 18.04 LTS, Ubuntu 20.04 LTS, Ubuntu 22.04 LTS, Ubuntu 22.10, CentOS, Debian, and RHEL are supported.

    * Ensure the user, with which you are connecting, has one of these shells set: `bash`, `dash`, `fish`, `csh`, `tcsh`, `ksh`, `zsh`.

On Ubuntu, ‘sh’ is aliased to `dash`.

    * The following utilities must be available: `tar`, `wget` (or `curl`), `dd`, `chmod`, `test`, `mkdir`, `echo`, `mv`, `uname`, `command`, and `gzip`.

    * The `$HOME` environment variable needs to be set correctly. The `$HOME/.cache` folder needs to be writable by the user with which you’re connecting.

    * We support the Alpine version 3.18. Ensure you have the following packages installed on the host beforehand: `libxext`, `libxrender`, `libxtst`, `libxi`, `freetype`, `procps`, `gcompat`.

Check the following command example:

`apk add libxext libxrender libxtst libxi freetype procps gcompat`

  * OpenSSH server, version 7.9p1 or later is recommended. Other SSH servers fully implementing RFC 4254 may work too, yet are not supported. SSH port forwarding must be enabled in server configuration.

  * The server needs to have at least 50 Mbps downstream capacity from the internet.

  * The connection between client and server should have at least 20 Mbps bandwidth, and no more than 200ms latency.

  * Single tenancy within a server or container.



