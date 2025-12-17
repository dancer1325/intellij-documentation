[//]: # (Source: https://www.jetbrains.com/help/idea/docker-images.html)
[//]: # (Downloaded: 2025-12-17 19:25:10)

## Manage Docker images in the Services tool window

IntelliJ IDEA lists all images that you pull or build locally in the Services tool window under the Images node of the corresponding Docker daemon connection. For more information, refer to [Images](services-tool-window.html#docker-images).

Select an image to view its name, ID, size, tags, date of last changes, and containers that are using this image. You can create a new container from the selected image, push the image to a configured Docker registry, or view the layers used by the image. Click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg) to see more actions: copy the image ID to the clipboard, run the [docker image inspect](https://docs.docker.com/engine/reference/commandline/image_inspect/) command, or show [labels](https://docs.docker.com/config/labels-custom-metadata/) applied to the image.

![Docker image properties](https://resources.jetbrains.com/help/img/idea/2025.3/55_DockerFindImage.png)

Images with no tags `<none>:<none>` can be one of the following:

  * Intermediate images that serve as layers for other images and don't take up any space.

  * Dangling images that remain when you rebuild an image based on a newer version of another image. You should regularly prune dangling images to preserve disk space.




To hide untagged images from the list, click ![The Filter menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) on the Docker toolbar and remove the checkmark from Untagged Images.

To delete one or several images, select them in the list and click ![The Delete Image button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg).

### Explore Docker images

  1. In the Services tool window, under Images, select the image you're interested in.

  2. In the Dashboard tab, click Show Layers.

  3. The Layers tab shows all layers that make up this image with details about each layer. Click Analyze image for more information to gather detailed information including changes to the image's file system.




You can double-click or right-click any file in an image's layer to open a copy of it in the editor if IntelliJ IDEA supports this file type, or download a copy of the file to your local file system if IntelliJ IDEA doesn't support this file type.

![Open a file from a Docker layer](https://resources.jetbrains.com/help/img/idea/2025.3/docker_explore_image_layers_open_file.png)
