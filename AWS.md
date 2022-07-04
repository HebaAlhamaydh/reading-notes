## AWS Cloud Servers
## What is an Amazon EC2 instance?
An Amazon EC2 instance is a virtual server in Amazon Elastic Compute Cloud (EC2) for running applications on the Amazon Web Services (AWS) infrastructure.
Amazon provides various types of instances with different configurations of CPU, memory, storage and networking resources to suit user needs
## Use Cases
- Run cloud-native and enterprise applications
- Scale for HPC applications
- Develop for Apple platforms
- Train and deploy ML applications
# Elastic Beanstalk
AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications. You can simply upload your code and it automatically handles the deployment. At the same time, you retain full control over the Amazon Web Services resources powering your application.
## Benefits
- Fast and simple to begin
- Developer productivity
- Impossible to outgrow
- Complete resource control
#  difference between T2 Micro and XL:
- T2 instances are a low-cost, general purpose instance type that provides a baseline level of CPU performance with the ability to burst above the baseline when needed.

- X1 Instances are a part of the Amazon EC2 memory-optimized instance family and are designed for running large-scale and in-memory applications in the AWS Cloud.

- Compared to other EC2 instances, X1 instances have one of the lowest price per GiB of RAM, and are ideal for running in-memory databases like SAP HANA, big data processing engines like Apache Spark or Presto, and high-performance computing (HPC) applications.
## Elastic Beanstalk
It is an easy to use service that deploys manages and scales web apps and services for you.
# Relationship Between EC2 and Elastic Beanstalk:
Elastic Beanstalk is one layer of abstraction away from the EC2 layer. Elastic Beanstalk will setup an "environment" for you that can contain a number of EC2 instances, an optional database, as well as a few other AWS components such as a Elastic Load Balancer, Auto-Scaling Group, Security Group.
## Benefits of Using Elastic Beanstalk:
- Timesaving server configuration.
- Powerful customization.
- Cost-effective price point.