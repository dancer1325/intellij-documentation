[//]: # (Source: https://www.jetbrains.com/help/idea/create-amazon-redshift-data-source-with-okta.html)
[//]: # (Downloaded: 2025-12-17 19:22:46)

## Prerequisites

  * Your Amazon Redshift dashboard must have a Amazon Redshift cluster in it. For more information about the Amazon Redshift cluster, refer to [Getting Started with Amazon Redshift.](https://docs.aws.amazon.com/redshift/latest/gsg/getting-started.html)

  * [AWS SSO](https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html) has to be enabled for your AWS account.

  * Your AWS account has to be [linked to your Okta account](https://docs.aws.amazon.com/singlesignon/latest/userguide/tutorials.html).

  * Before connecting to a Amazon Redshift database with Okta SSO authentication, make sure to install and set up the [Okta Verify](https://help.okta.com/en-us/content/topics/mobile/okta-verify-overview.htm) application first.

Once the required software is set up and ready, you need to create a Amazon Redshift data source in IntelliJ IDEA and configure it to use it with Okta SSO authentication. 



