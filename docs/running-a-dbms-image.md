[//]: # (Source: https://www.jetbrains.com/help/idea/running-a-dbms-image.html)
[//]: # (Downloaded: 2025-12-17 19:59:13)

# Run a database in a Docker container

You can use Docker to run a database in a container as if it were a remote server, and test how your application interacts with it. This tutorial describes how to run a Docker container with a PostgreSQL server and connect to it using IntelliJ IDEA.

Before you begin, install and run Docker, enable the Docker plugin, and connect to the Docker daemon in IntelliJ IDEA. For more information, refer to [Getting started with Docker in IntelliJ IDEA](docker.html#connect_to_docker).

For database management features, refer to [Database Tools and SQL](relational-databases.html).

### Pull a PostgreSQL server image

  1. In the Services tool window, expand your Docker connection and select the Images node.

  2. In the Image to pull field, start typing `postgres` and select the necessary image repository. For example, select `postgres` to pull the default `postgres:latest` image.

  3. Press `Ctrl+Enter` and wait until Docker pulls the image.


![Pull the Docker image with PostgreSQL](https://resources.jetbrains.com/help/img/idea/2025.3/docker_postgres_pull.png)

### Run a container from the PostgreSQL server image

  1. Expand the Images node, select the PostgreSQL server image, and click ![The Create Container button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Create Container.

![Select the PostgreSQL image and click Create Container](https://resources.jetbrains.com/help/img/idea/2025.3/docker_postgres_create_container.png)
  2. In the Create Docker Configuration dialog, do the following:

     * Click Modify options and select Randomly publish all exposed ports to publish all exposed container ports to the host interfaces. For a more secure setup, you will need to define specific port bindings, of course. However, in this tutorial, we assume that your local machine is secure enough and there is nothing important.

     * Click Modify options, select Environment variables, and configure environment variables that define the authentication settings for your PostgreSQL server. For the purposes of this tutorial, we can use [Trust Authentication](https://www.postgresql.org/docs/current/auth-trust.html). Keep in mind that this will enable anyone who can connect to the PostgreSQL server to access the database with any username of their choice. In the Environment variables field, click ![The Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.menu-open.svg) and add the `POSTGRES_HOST_AUTH_METHOD` variable with the value `trust`.

For more information about authenticating, see the [official PostgreSQL Docker Hub image page](https://hub.docker.com/_/postgres).

Optionally, you can specify custom names for the configuration and the container.


![The Create Docker Configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/docker_postgresql_create_configuration.png)

### Connect to the PostgreSQL server

Docker automatically maps the default PostgreSQL server port 5432 in the container to a host port within the ephemeral port range (typically from 32768 to 61000). This tutorial assumes that port 32768 was used. To check what the actual mapping is, right-click the PostgreSQL container in the Services tool window under the Containers node, click Inspect, and then find the value of the `HostPort` field in the Inspection output.

  1. Open the Database tool window (View | Tool Windows | Database).

  2. Click ![The New button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Data Source | PostgreSQL.

  3. Set the host name to `localhost`, the port number to `32768` (or whatever host port it was mapped to), the default database and user to `postgres`. No password is required since we used `trust` authentication to run the PostgreSQL server.

  4. If necessary, download the driver and test the connection.

  5. Click OK to add the PostgreSQL server as a data source.




For more information about working with database sources in IntelliJ IDEA, refer to [Database Tools and SQL](relational-databases.html).

10 January 2025

[Docker Compose](docker-compose.html)[Dockerize a Java application](dockerize-java-app.html)
