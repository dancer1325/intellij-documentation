[//]: # (Source: https://www.jetbrains.com/help/idea/big-data-tools-hdfs.html)
[//]: # (Downloaded: 2025-12-17 19:19:03)

## Samples of Hadoop File System configuration files

Type| Sample configuration  
---|---  
HDFS|  <?xml version="1.0"?> <configuration> <property> <name>fs.hdfs.impl</name> <value>org.apache.hadoop.hdfs.DistributedFileSystem</value> </property> <property> <name>fs.defaultFS</name> <value>hdfs://example.com:9000/</value> </property> </configuration>  
S3|  <?xml version="1.0"?> <configuration> <property> <name>fs.s3a.impl</name> <value>org.apache.hadoop.fs.s3a.S3AFileSystem</value> </property> <property> <name>fs.s3a.access.key</name> <value>sample_access_key</value> </property> <property> <name>fs.s3a.secret.key</name> <value>sample_secret_key</value> </property> <property> <name>fs.defaultFS</name> <value>s3a://example.com/</value> </property> </configuration>  
WebHDFS|  <?xml version="1.0"?> <configuration> <property> <name>fs.webhdfs.impl</name> <value>org.apache.hadoop.hdfs.web.WebHdfsFileSystem</value> </property> <property> <name>fs.defaultFS</name> <value>webhdfs://master.example.com:50070/</value> </property> </configuration>  
WebHDFS and Kerberos|  <?xml version="1.0"?> <configuration> <property> <name>fs.webhdfs.impl</name> <value>org.apache.hadoop.hdfs.web.WebHdfsFileSystem</value> </property> <property> <name>fs.defaultFS</name> <value>webhdfs://master.example.com:50070</value> </property> <property> ​ <name>hadoop.security.authentication</name> <value>Kerberos</value> </property> <property> <name>dfs.web.authentication.kerberos.principal</name> <value>testuser@EXAMPLE.COM</value> </property> <property>​ <name>hadoop.security.authorization</name>​ <value>true</value>​ </property> </configuration>
