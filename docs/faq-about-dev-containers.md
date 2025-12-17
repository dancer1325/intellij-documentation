[//]: # (Source: https://www.jetbrains.com/help/idea/faq-about-dev-containers.html)
[//]: # (Downloaded: 2025-12-17 19:26:44)

## I see various volumes and properties in Docker after I created a Dev Container. What does each of them do?

After a Dev Container is created, the following volumes and properties appear in Docker:

  * `jb_devcontainers_shared_volume`: the process of copying an IDE backend takes a certain amount of time. However, this process is done only once during the first Dev Container creation, and everything is copied into this volume. Then, this volume is shared among multiple containers, and we don't need to repeat the downloading process. If we create a Dev Container using another IDE or a different IDE version, we copy it into the same Docker volume. All backends are stored in one volume, making it easy to manage. 

For example, remove unnecessary backends through the Manage backends dialog.

  * `jb-devcontainer-features-xxx`: if you use `features` in your `devcontainer.json` file then all features are placed into such images. 

Currently, the unnecessary images should be deleted manually.

  * `jb_devcontainer_sources_xxx`: if we use `git clone` then all sources are cloned into this volume using helper container (based on alpine/git image).



