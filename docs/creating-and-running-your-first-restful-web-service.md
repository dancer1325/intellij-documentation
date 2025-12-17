[//]: # (Source: https://www.jetbrains.com/help/idea/creating-and-running-your-first-restful-web-service.html)
[//]: # (Downloaded: 2025-12-17 19:23:27)

## Troubleshooting

### Compatibility with Jakarta EE

If you get a `404` error, make sure you have selected the Jakarta EE specification version that is compatible with your version of GlassFish when [creating the project](#new_project).

For more information, refer to the [GlassFish version compatibility](https://github.com/eclipse-ee4j/glassfish#compatibility).

### Older IntelliJ IDEA versions

If you are using IntelliJ IDEA version 2020.2.2 or earlier, the New Project wizard will not add all of the necessary dependencies required for Tomcat. In this case, open pom.xml and add the following dependencies:

<dependency> <groupId>org.glassfish.jersey.media</groupId> <artifactId>jersey-media-json-jackson</artifactId> <version>2.31</version> </dependency> <dependency> <groupId>org.glassfish.jersey.inject</groupId> <artifactId>jersey-hk2</artifactId> <version>2.31</version> </dependency>

For example, in version 2020.2.3, the generated pom.xml looks like this:

<?xml version="1.0" encoding="UTF-8"?> <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <groupId>com.example</groupId> <artifactId>RestTomcatHelloWorld</artifactId> <version>1.0-SNAPSHOT</version> <name>RestTomcatHelloWorld</name> <packaging>war</packaging> <properties> <maven.compiler.target>1.8</maven.compiler.target> <maven.compiler.source>1.8</maven.compiler.source> <junit.version>5.6.2</junit.version> </properties> <dependencies> <dependency> <groupId>javax.ws.rs</groupId> <artifactId>javax.ws.rs-api</artifactId> <version>2.1.1</version> <scope>provided</scope> </dependency> <dependency> <groupId>org.glassfish.jersey.containers</groupId> <artifactId>jersey-container-servlet</artifactId> <version>2.31</version> </dependency> <dependency> <groupId>org.glassfish.jersey.media</groupId> <artifactId>jersey-media-json-jackson</artifactId> <version>2.31</version> </dependency> <dependency> <groupId>org.glassfish.jersey.inject</groupId> <artifactId>jersey-hk2</artifactId> <version>2.31</version> </dependency> <dependency> <groupId>org.glassfish.jersey.core</groupId> <artifactId>jersey-client</artifactId> <version>2.31</version> </dependency> <dependency> <groupId>org.junit.jupiter</groupId> <artifactId>junit-jupiter-api</artifactId> <version>${junit.version}</version> <scope>test</scope> </dependency> <dependency> <groupId>org.junit.jupiter</groupId> <artifactId>junit-jupiter-engine</artifactId> <version>${junit.version}</version> <scope>test</scope> </dependency> </dependencies> <build> <plugins> <plugin> <groupId>org.apache.maven.plugins</groupId> <artifactId>maven-war-plugin</artifactId> <version>3.3.0</version> </plugin> </plugins> </build> </project>
