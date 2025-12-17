[//]: # (Source: https://www.jetbrains.com/help/idea/connect-to-registries.html)
[//]: # (Downloaded: 2025-12-17 19:22:17)

# Connect to container registries

Currently, IntelliJ IDEA supports connection to a Google Artifact registry that can be used for storing and managing Docker container images in Google Cloud.

### Configure the Google Artifact registry connection

  1. Install Google Cloud CLI using the [interactive installer](https://cloud.google.com/sdk/docs/downloads-interactive).

  2. Initialize Google Cloud CLI using the following command: 

gcloud init 

  3. Configure [authentication](https://cloud.google.com/artifact-registry/docs/docker/authentication#gcloud-helper) with user credentials using the following command: 

gcloud auth login 

  4. Configure the `~/.docker/config.json` file using the `gcloud auth configure-docker` command and the project's region. 

Check the following example:

gcloud auth configure-docker europe-west10-docker.pkg.dev 

  5. Using the `docker-credential-gcloud` utility, request credentials for the repository in the terminal: 

$ echo "https://europe-west10-docker.pkg.dev" | docker-credential-gcloud get { "Secret": "...", "Username": "_dcgcloud_token" } 

  6. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Docker | Docker Registry.

  7. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add the new Docker registry and specify the following information: 

     * Registry: select Docker V2 as the registry type.

     * Address: specify the configured project's region (for example, `https://europe-west10-docker.pkg.dev`)

     * Username: specify the [username](#utility) requested from the `docker-credential-gcloud` utility.

     * Password: specify the [password](#utility) requested from the `docker-credential-gcloud` utility

Test the connection and click OK.

  8. Under the Docker Registries node you should be able to see the images from the repositories associated with the configured region (such as `europe-west10`).




25 March 2025

[Troubleshooting Dev Container issues](troubleshooting-dev-containers.html)[Dev Container CLI](dev-container-cli.html)
