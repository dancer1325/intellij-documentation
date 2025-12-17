[//]: # (Source: https://www.jetbrains.com/help/idea/terraform.html)
[//]: # (Downloaded: 2025-12-17 20:04:10)

## Run Terraform

The Terraform and HCL plugin provides dedicated run configurations for Terraform. These run configurations allow you to customize the execution of `terraform` commands, such as adding arguments or passing environment variables.

### Run Terraform using gutter icon

  1. In a Terraform file, click ![Run](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.run.svg) in the gutter.

  2. In the window that opens, select either Plan to create an execution plan or Apply if you already have a Terraform plan and want to apply it.

![Terraform run from gutter](https://resources.jetbrains.com/help/img/idea/2025.3/terraform_run.png)



If the Terraform initialization step was not performed for this directory, there will be a warning sign in the Run gutter icon. In this case, IntelliJ IDEA suggests you running the `terraform init` command before running `terraform plan` or `terraform apply`.

Running Terraform from the gutter icon creates a temporary run configuration. You can save it as a permanent one by clicking ![More Actions](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) in the run widget and selecting Save Configuration.

### Create Terraform run configuration manually

  1. Go to Run | Edit Configurations. Alternatively, press `Alt+Shift+F10`, then `0`. 

  2. Click the Add New Configuration button (![Add a run/debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and start typing Terraform.

![Terraform run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/terraform_run_configuration.png)
  3. Select a type of the run configuration:

     * Terraform Init to run `terraform init` commands

     * Terraform Validate to run `terraform validate` commands

     * Terraform Plan to run `terraform plan` commands

     * Terraform Apply to run `terraform apply` commands

     * Terraform Destroy to run `terraform destroy` commands

     * Terraform, which lets you provide any other Terraform command

  4. In the Command list, select a Terraform command. To run a command not included in this list, select Custom and specify it in the Program arguments field.

  5. Give the run configuration a name and, if necessary, change the working directory. If you use environment variables, specify them in the Environment variables field or select a file to use variables from it.



