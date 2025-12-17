[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-kerberos.html)
[//]: # (Downloaded: 2025-12-17 19:19:07)

# Kerberos

Kerberos is a network authentication protocol that provides a secure way to authenticate clients and servers over an insecure network.

The [Big Data Tools plugins](https://plugins.jetbrains.com/bundles/8-big-data-tools) allow you to use Kerberos to authenticate connections to [Kafka](big-data-tools-kafka.html), [HDFS](big-data-tools-hdfs.html), and [Hive Metastore](big-data-tools-hive.html).

### Use Kerberos to authenticate in Kafka

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Kafka. Or, if you want to edit an existing connection, select it and click ![Edit a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg).

  2. Open the Kerberos settings: In the Configuration source, select Custom, and, under Authentication, select SASL | Kerberos.

  3. If you want to use the Kerberos ticket cache created by the [kinit](https://web.mit.edu/kerberos/krb5-1.12/doc/user/user_commands/kinit.html) tool, select Use kinit cache.

Otherwise, clear the Use kinit cache checkbox and provide authentication data:

     * In the Principal box, enter your Kerberos principal, such as john@EXAMPLE.ORG.

     * In the Keytab box, specify a path to the [keytab](https://web.mit.edu/kerberos/krb5-devel/doc/basic/keytab_def.html) file.

  4. Click IDE Kerberos settings. In the window that opens, in the Krb5 config field, specify your krb5.conf or krb5.ini file or keep the default one.

The path to a krb5.conf file is a global setting. It applies to all other connections that use Kerberos in your IDE. You can also access global Kerberos settings in Settings | Appearance & Behavior | System Settings | Kerberos Authentication.




Alternatively, you can set up Kerberos connection using configuration properties. Switch to Properties in Configuration source and add the needed properties, for example:

sasl.kerberos.service.name=kafka security.protocol=SASL_PLAINTEXT sasl.mechanism=GSSAPI sasl.jaas.config=com.sun.security.auth.module.Krb5LoginModule required useKeyTab=true keyTab="/etc/security/keytabs/john.keytab" principal="john@EXAMPLE.COM"; 

### Use Kerberos to authenticate in HDFS

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select HDFS. Or, if you want to edit an existing connection, select it and click ![Edit a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg).

  2. Open the Kerberos settings: In the Configuration source, select Custom, and, under Authentication, select Kerberos.

  3. If you want to use the Kerberos ticket cache created by the [kinit](https://web.mit.edu/kerberos/krb5-1.12/doc/user/user_commands/kinit.html) tool, select Use kinit cache.

Otherwise, in the Authentication by list, select the authentication method:

     * Keytab: enter your Kerberos principal, such as john@EXAMPLE.ORG, and a path to the [keytab](https://web.mit.edu/kerberos/krb5-devel/doc/basic/keytab_def.html) file.

     * Password: enter your Kerberos principal, such as john@EXAMPLE.ORG, and the principal password.

     * JAAS config: specify the path to the [JAAS Login Configuration File](https://docs.oracle.com/javase/7/docs/technotes/guides/security/jgss/tutorials/LoginConfigFile.html). IntelliJ IDEA detects JAAS entries in the file, and you can then select the one you want to use for authentication in the JAAS entry list. Alternatively, click Generate JAAS entry to generate a new JAAS entry and add it to the file.

The path to a JAAS Login Configuration File is a global setting. It applies to all HDFS connections that use Kerberos in your IDE.

  4. Click IDE Kerberos settings. In the window that opens, in the Krb5 config field, specify your krb5.conf or krb5.ini file or keep the default one.

The path to a krb5.conf file is a global setting. It applies to all other connections that use Kerberos in your IDE. You can also access global Kerberos settings in Settings | Appearance & Behavior | System Settings | Kerberos Authentication.




### Use Kerberos to authenticate in Hive

  1. In the Big Data Tools window, click ![Add a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select Hive Metastore. Or, if you want to edit an existing connection, select it and click ![Edit a connection](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg).

  2. Open the Kerberos settings: In the Configuration source, select Custom, and, under Authentication, select Kerberos.

  3. If you want to use the Kerberos ticket cache created by the [kinit](https://web.mit.edu/kerberos/krb5-1.12/doc/user/user_commands/kinit.html) tool, select Use kinit cache.

Otherwise, clear the Use kinit cache checkbox and provide authentication data:

     * In the Principal box, enter your Kerberos principal, such as john@EXAMPLE.ORG.

     * In the Keytab box, specify a path to the [keytab](https://web.mit.edu/kerberos/krb5-devel/doc/basic/keytab_def.html) file.

  4. Click IDE Kerberos settings. In the window that opens, in the Krb5 config field, specify your krb5.conf or krb5.ini file or keep the default one.

The path to a krb5.conf file is a global setting. It applies to all other connections that use Kerberos in your IDE. You can also access global Kerberos settings in Settings | Appearance & Behavior | System Settings | Kerberos Authentication.




### Enable debug logging

If you have issues with Kerberos authentication, you can enable logging of Kerberos and Java Generic Security Services (JGSS) debug messages. The logs are then available in Help | Show Log in Finder and Help | Open Log in Editor.

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Appearance & Behavior | System Settings | Kerberos Authentication.

  2. Select the Kerberos debug logging and JGSS debug logging checkboxes.




09 May 2025

[Zeppelin notebooks](big-data-tools-zeppelin-notebooks.html)[Data Science and ML tools](scientific-tools.html)
