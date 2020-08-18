## Adventure Works Sample Application

This repository contains a CloudFormation template file that is used to launch a sample application for the purpose of demonstrating the monitoring capabilities of CloudWatch Application Insights.

The template relies on two custom built AMI's to launch properly.
* A Windows AMI running SQL Server. This AMI is pre-configured with [Microsoft's AdventureWorks2016 sample database](https://github.com/microsoft/sql-server-samples/releases/tag/adventureworks "AdventureWorks databases")
* A Windows AMI running a .NET application that will be used to make calls to the database.


The CloudFormation template contains the following:
* Load balanced, auto-scaling group with EC2 instances running the sample .NET application.
* Windows SQL Server EC2 instance hosting the AdventureWorks database.
* VPC, security groups, route table, and other networking related infrastructure is all setup through this template.



## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

#####NOTE: This is a sample application to be used for demonstration purposes only.
This application was not built to be a legitimate enterprise application. Because of this, there are a few potential concerns we would like for you to be aware of.

* When launching the CloudFormation stack, we give the option for you to provide your own IP to be used for the security group ingress that allows RDP connections to your desktop. If this is not specified, the default is 0.0.0.0/0.
* Traffic to the web server is over HTTP.
## License

This library is licensed under the MIT-0 License. See the LICENSE file.

