[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-kafka.html)
[//]: # (Downloaded: 2025-12-17 19:19:06)

## Connect to Kafka

### Connect to Kafka using cloud providers

### Connect to Confluent cluster

  1. Open the Kafka tool window: View | Tool Windows | Kafka.

  2. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) (New Connection).

  3. In the Name field, enter the name of the connection to distinguish it between other connections.

  4. In the Configuration source list, select Cloud, and then, in the Provider list, select Confluent.

  5. Go to <https://confluent.cloud/home>. On the right side of the page, click the settings menu, select Environments, and select your cluster, and then select Clients | Java.

In the Copy the configuration snippet for your clients block, provide Kafka API keys and click Copy.

  6. Go back to your IDE and paste the copied properties into the Configuration field.

  7. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.


![Kafka Confluent](https://resources.jetbrains.com/help/img/idea/2025.3/kafka_confluent.png)

Optionally, you can set up:

  * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

  * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.




### Connect to AWS MSK cluster

  1. Open the Kafka tool window: View | Tool Windows | Kafka.

  2. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) (New Connection).

  3. In the Name field, enter the name of the connection to distinguish it between other connections.

  4. In the Configuration source list, select Cloud, and then, in the Provider list, select AWS MSK.

  5. In the Bootstrap servers field, enter the URL of the Kafka broker or a comma-separated list of URLs.

  6. In the AWS Authentication list, select the authentication method.

     * Default credential providers chain: use the credentials from the default provider chain. For more information about the chain, refer to [Using the Default Credential Provider Chain](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html).

     * Profile from credentials file: select a profile from your credentials file.

     * Explicit access key and secret key: enter your credentials manually.

  7. Optionally, you can [connect to Schema Registry](#connect_schema_registry).

  8. If you want to use an SSH tunnel while connecting to Kafka, select Enable tunneling and in the SSH configuration list, select an SSH configuration or create a new one.

  9. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.


![Kafka AWS MSK](https://resources.jetbrains.com/help/img/idea/2025.3/kafka_aws_msk.png)

Optionally, you can set up:

  * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

  * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.




### Connect to a custom Kafka server

  1. Open the Kafka tool window: View | Tool Windows | Kafka.

  2. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) (New Connection).

  3. In the Name field, enter the name of the connection to distinguish it between other connections.

  4. In the Configuration source list, select Custom.

  5. In the Bootstrap servers field, enter the URL of the Kafka broker or a comma-separated list of URLs.

  6. Under Authentication, select an authentication method:

     * None: connect without authentication.

     * SASL: select an SASL mechanism (Plain, SCRAM-SHA-256, SCRAM-SHA-512, or [Kerberos](big-data-tools-kerberos.html)) and provide your username and password.

     * SSL

       * Select Validate server host name if you want to verify that the broker host name matches the host name in the broker certificate. Clearing the checkbox is equivalent to adding the `ssl.endpoint.identification.algorithm=` property.

       * In the Truststore location, provide a path to the SSL truststore location (`ssl.truststore.location` property).

       * In the Truststore password, provide a path to the SSL truststore password (`ssl.truststore.password` property).

       * Select Use Keystore client authentication and provide values for Keystore location (`ssl.keystore.location`), Keystore password (`ssl.keystore.password`), and Key password (`ssl.key.password`).

     * AWS IAM: use AWS IAM for Amazon MSK. In the AWS Authentication list, select one of the following:

       * Default credential providers chain: use the credentials from the default provider chain. For more information about the chain, refer to [Using the Default Credential Provider Chain](https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/credentials.html).

       * Profile from credentials file: select a profile from your credentials file.

       * Explicit access key and secret key: enter your credentials manually.

  7. Optionally, you can [connect to Schema Registry](#connect_schema_registry).

  8. If you want to use an SSH tunnel while connecting to Kafka, select Enable tunneling and in the SSH configuration list, select an SSH configuration or create a new one.

  9. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.


![Kafka custom connection](https://resources.jetbrains.com/help/img/idea/2025.3/kafka_connect_custom.png)

Optionally, you can set up:

  * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

  * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.




### Connect to Kafka using properties

  1. Open the Kafka tool window: View | Tool Windows | Kafka.

  2. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) (New Connection).

  3. In the Name field, enter the name of the connection to distinguish it between other connections.

  4. In the Configuration source list, select Properties.

  5. In the Bootstrap servers field, enter the URL of the Kafka broker or a comma-separated list of URLs.

  6. Select the way to provide Kafka Broker configuration properties:

     * Implicit: paste provided configuration properties. Or you can enter them manually using code completion and quick documentation that IntelliJ IDEA provides.

     * From File: select the properties file.

  7. Optionally, you can [connect to Schema Registry](#connect_schema_registry).

  8. If you want to use an SSH tunnel while connecting to Kafka, select Enable tunneling and in the SSH configuration list, select an SSH configuration or create a new one.

  9. Once you fill in the settings, click Test connection to ensure that all configuration parameters are correct. Then click OK.




Optionally, you can set up:

  * Enable connection: clear the checkbox if you want to disable this connection. By default, the newly created connections are enabled.

  * Per project: select to enable these connection settings only for the current project. Clear the checkbox if you want this connection to be visible in other projects.




### Connect to Kafka in a Spring project

If you use Kafka in a Spring project, you can quickly connect to a Kafka cluster (or open an existing connection) based on the configuration properties from your application properties file.

  1. Open your application.properties or application.yml file with at least the `bootstrap-servers` property defined.

  2. In the gutter, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.providers.kafka.png) and select Create Kafka connection. If you have already configured Kafka connections, you can also select them in this list.


![Kafka properties in Spring](https://resources.jetbrains.com/help/img/idea/2025.3/spring_connect_kafka.png)

Additionally, if you have a method annotated with `@KafkaListener`, you can click ![](https://resources.jetbrains.com/help/img/idea/2025.3/product.icons.gutter.messageQueueReceiver.svg) next to it to quickly produce messages to the specified topic or consume data from them.
