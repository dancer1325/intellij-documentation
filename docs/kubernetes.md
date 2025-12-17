[//]: # (Source: https://www.jetbrains.com/help/idea/kubernetes.html)
[//]: # (Downloaded: 2025-12-17 19:31:01)

## Resource configuration files

The Kubernetes plugin provides rich support for resource configuration files in YAML, and only basic support for the JSON format.

### Supported features

Feature| YAML| JSON  
---|---|---  
[Auto-completion](auto-completing-code.html)| Supported| Supported  
[Quick documentation](viewing-reference-information.html#inline-quick-documentation)| Supported| Supported  
[Inspections and quick fixes](code-inspection.html)| 

  * Invalid, missing, and duplicated keys
  * Non-editable (read-only) keys and resources
  * Deprecated keys and resources
  * Invalid integer and enum key values

| 

  * Invalid, missing, and duplicated properties

  
[Live templates](using-live-templates.html)| Predefined templates for common resource kinds| No predefined live templates  
[Smart completion](advanced-code-completion.html#invoke_smart_completion)| Supported| Not supported  
[Custom resource definitions](#crd)| Supported| Not supported  
Label definitions and selectors| Navigation using gutter icons, find usages, and renaming| Not supported  
Enhancements of the original Kubernetes model| Enums instead of plain strings where applicable| None  
  
IntelliJ IDEA recognizes Kubernetes resource configuration files using the following mandatory fields:

  * `apiVersion`: identifies the versioned schema of the object representation

  * `kind`: identifies the resource type (for example, `Service`, `Pod`, `Deployment`, and so on)




If both of the previous fields are present in a YAML or JSON file, IntelliJ IDEA will mark the file with the corresponding Kubernetes icon and enable all available features.

### Create a resource file

With IntelliJ IDEA, you can quickly create configuration files for some of the most popular resources in Kubernetes.

  1. In the Project tool window `Alt+1`, right-click a folder, select New or press `Alt+Insert`, and then select Kubernetes Resource.

  2. In the Name field, type your resource name and select the file template from the list.

![New Kubernetes Resource Window](https://resources.jetbrains.com/help/img/idea/2025.3/kubernetes_new_resource.png)

This will create a new file with its contents based on the selected [file template](using-file-and-code-templates.html).




Alternatively, in YAML files, you can use predefined [live templates](using-live-templates.html), for example:

  * `kconfigmap`: Kubernetes ConfigMap

  * `kcronjob`: Kubernetes CronJob

  * `kdeployment`: Kubernetes Deployment

  * `kingress`: Kubernetes Ingress

  * `kpod`: Kubernetes Pod

  * `kresource`: Kubernetes Resource from Scratch

  * `kservice`: Kubernetes Service


![Kubernetes live templates](https://resources.jetbrains.com/help/img/idea/2025.3/kubernetes_live_templates.png)

To view the list of all live templates for Kubernetes resources, edit them or create new ones, open the Settings dialog `Ctrl+Alt+S`, select Editor | Live Templates, and expand the Kubernetes group in the list.

When you open a Kubernetes resource file in the editor, IntelliJ IDEA displays [inlay hints](inlay-hints.html) and a floating toolbar with the most popular actions, including:

  1. A floating toolbar where you can:

     * Select the current cluster and namespace

     * ![Apply icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.actions.deploy.svg) Apply the changes and deliver them to the current cluster

     * ![Delete icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.actions.undeploy.svg) Delete the resource

     * ![Compare icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.diff.svg) Compare the changes with the cluster version

     * ![Reload icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.refresh.svg) Reload content from the cluster

![Floating toolbar](https://resources.jetbrains.com/help/img/idea/2025.3/k8s-floating-toolbar.png)
  2. Inlay hints to check the [statuses of deployed resources](#view-resource-info)

  3. Inlay hints to [reveal and copy values of referenced secrets](#inlay-hints-secrets)

  4. Inlay hints to [forward ports](#forward-ports)


![Hints in Kubernetes manifests](https://resources.jetbrains.com/help/img/idea/2025.3/k8s-yaml-editor-hints.png)

You can change the appearance of inlay hints to display only icons. Right-click an inlay hint and select the Icons only option from the context menu. Deselect the option to bring back the default appearance with captions.

### Configure the floating toolbar appearance

You can configure when to display the floating toolbar in the editor.

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Kubernetes.

  2. Use the Show floating toolbar in editor option to choose when the floating toolbar appears: 

     * Always show

     * Show when Mouse Moves

     * Don't show

Alternatively, you can right-click the floating toolbar and select the required option.




### Disable Kubernetes schema validation

IntelliJ IDEA validates your Kubernetes files against the Kubernetes API schema. This includes checking it for required keys or possible types of resource.

If your file contains `apiVersion` and `kind`, but it is not a Kubernetes file, you can disable such validation. You can suppress inspections and change their scope and severity in Settings | Editor | Inspections | Kubernetes. Or you can mark a file with a special directive to disable validation in it:

  * At the beginning of the file, add `# nonk8s`.

  * Alternatively, if you already have a warning about an unknown resource, right-click it in the Problems tool window and select Show Quick-Fixes | Mark this file as non-Kubernetes.



