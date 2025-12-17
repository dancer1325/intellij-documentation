[//]: # (Source: https://www.jetbrains.com/help/idea/debugging-in-kubernetes.html)
[//]: # (Downloaded: 2025-12-17 19:24:22)

## Ephemeral containers

IntelliJ IDEA supports attaching [ephemeral containers](https://kubernetes.io/docs/concepts/workloads/pods/ephemeral-containers/) to running pods without restarting them. This way, you can inspect a live Kubernetes environment, run diagnostic commands, and investigate issues directly inside a running pod.

An ephemeral container is temporarily added to an existing pod for debugging and runs alongside your application containers. For this purpose, IntelliJ IDEA runs the `kubectl debug` command under the hood. You can either attach your custom debug container or use a lightweight BusyBox image, which provides common tools like `ping`, `netstat`, `wget`, and `top` out of the box.

For more details on debugging running pods, refer to the [Kubernetes documentation](https://kubernetes.io/docs/tasks/debug/debug-application/debug-running-pod/).

### Attach BusyBox to a running pod

  1. Open the [Services](services-tool-window.html) tool window: select View | Tool Windows | Services or press `Alt+8`.

  2. Expand the node that lists running pods, right-click the pod you want to debug, and select Ephemeral Debug Containers | Attach Busybox from the context menu.

Alternatively, select the required pod, click ![the Ephemeral Container icon](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-kubernetes.icons.newui.ephemeralStoppedContainer.png) on the toolbar, and select Attach Busybox from the dropdown.

![Attach BusyBox](https://resources.jetbrains.com/help/img/idea/2025.3/kubernetes_attach_busybox_container.png)



### Attach a custom container to a running pod

  1. Open the [Services](services-tool-window.html) tool window: select View | Tool Windows | Services or press `Alt+8`.

  2. Expand the node that lists running pods, right-click the pod you want to debug, and select Ephemeral Debug Containers | Attach Custom from the context menu.

Alternatively, select the required pod, click ![the Ephemeral Container icon](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-kubernetes.icons.newui.ephemeralStoppedContainer.png) on the toolbar, and select Attach Custom from the dropdown.

  3. In the Attach Custom Debug Container dialog, use the following fields to customize the `kubectl debug` command for starting and attaching an ephemeral container:

     * Pod: select the pod you want to debug from the dropdown.

     * Target: specify the target container inside the selected pod.

     * Image: start typing the name of an image to use for debugging and then select it from the list of suggestions.

     * Executable: specify an absolute path to the shell to run inside the ephemeral container after it starts (for example, `/bin/sh` for BusyBox or `/bin/bash` for Ubuntu).

     * Options: provide additional configuration parameters for the debug container. For examples, refer to the [Kubernetes documentation](https://kubernetes.io/docs/reference/kubectl/generated/kubectl_debug/).

![the Attach Custom Debug Container dialog](https://resources.jetbrains.com/help/img/idea/2025.3/kubernetes_attach_custom_container.png)

Hover over the ![the Preview Command](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-kubernetes.icons.newui.consoleCommand.png) icon to preview the resulting `kubectl debug` command.

  4. Click Attach to Pod.




When IntelliJ IDEA starts a new ephemeral container and successfully attaches it to the pod, the Console tab opens, where you can run commands and inspect the pod.

![Debug console](https://resources.jetbrains.com/help/img/idea/2025.3/kubernetes_busybox_container_console.png)

If you [attach BusyBox](#attach-busybox-container-to-pod), IntelliJ IDEA automatically uses `sh`. For [custom images](#attach-custom-container-to-pod), the IDE uses the shell specified in the Executable field.

The container is removed when you delete the pod it is attached to.

### Recent commands

When you attach an ephemeral container using the Ephemeral Debug Containers menu, IntelliJ IDEA automatically saves the corresponding `kubectl debug` command. You can access and rerun it later from the Recent section.

![Recent commands](https://resources.jetbrains.com/help/img/idea/2025.3/kubernetes_recent_commands.png)

### Start an ephemeral container using a recent command

  1. Open the [Services](services-tool-window.html) tool window: select View | Tool Windows | Services or press `Alt+8`.

  2. Expand the node that lists running pods and right-click the pod you want to debug. Select Ephemeral Debug Containers and the required recent command from the context menu.

Alternatively, select the required pod, click ![the Ephemeral Container icon](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-kubernetes.icons.newui.ephemeralStoppedContainer.png) on the toolbar, and select the recent command from the dropdown.




### Manage recent commands

  1. Access recent commands:

     * In the Settings dialog (`Ctrl+Alt+S`) , select Build, Execution, Deployment | Kubernetes.

     * Open the Sevices tool window (`Alt+8`). Right-click any running pod and select Ephemeral Debug Containers | Edit Recents from the context menu.

  2. Navigate to the Ephemeral Debug Containers section.

     * To add a new command that you can preconfigure and quickly start new ephemeral containers, click ![the Plus icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg). In the Add Debug Parameters dialog, you can specify an image, executable, and options for the `kubectl debug` command.

     * To remove a command from recents, select it in the table and click ![the Minus icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.remove.svg).

     * To edit an existing command, select it in the table and click ![the Edit icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg). In the Add Debug Parameters dialog, change the image, executable, and options for the `kubectl debug` command.



