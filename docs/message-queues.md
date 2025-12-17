[//]: # (Source: https://www.jetbrains.com/help/idea/message-queues.html)
[//]: # (Downloaded: 2025-12-17 19:32:21)

# Message queues

A message queue provides asynchronous communication between your application components. This means that the sender and receiver of the message don't interact with each other directly and don't need to interact with the message queue at the same time.

The Java Message Service (JMS) framework is a messaging standard for Java application components. IntelliJ IDEA provides [code completion](auto-completing-code.html) and navigation for several JMS provider implementations:

  * [Apache ActiveMQ](https://activemq.apache.org/)

  * [Apache Kafka](https://kafka.apache.org/)

  * [RabbitMQ](https://www.rabbitmq.com/)




When implementing the sender method, you can press `Ctrl+Space` to complete available destinations and then hold `Ctrl` while clicking it to navigate to the relevant declaration.

![RabbitMQ exchange completion](https://resources.jetbrains.com/help/img/idea/2025.3/rabbitmq-exchange.png)

Click ![The message queue receiver icon](https://resources.jetbrains.com/help/img/idea/2025.3/product.icons.gutter.messageQueueReceiver.svg) in the gutter where you implemented the receiver (listener) method to list all usages of the corresponding destination and navigate to any one of them.

![RabbitMQ receiver gutter icon](https://resources.jetbrains.com/help/img/idea/2025.3/rabbitmq-receiver-gutter.png)

IntelliJ IDEA recognizes queue names as references and provides corresponding coding assistance including navigation and refactoring. If it's not the case, press `Alt+Enter` on a destination, select Inject language or reference, and select a message broker.

28 August 2024

[Micronaut](micronaut.html)[OpenRewrite](openrewrite.html)
