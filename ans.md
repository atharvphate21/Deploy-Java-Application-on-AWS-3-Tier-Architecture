“In this project, I implemented a production-style Java application deployment on AWS using a 3-tier architecture approach. The main goal was to build a scalable, secure, and highly available infrastructure similar to real-world enterprise environments.

The architecture was divided into three layers: presentation tier, application tier, and database tier.

In the presentation tier, I used Nginx web servers behind a public-facing Load Balancer. Nginx acted as a reverse proxy and handled incoming HTTP requests. For better scalability and availability, the Nginx servers were deployed in an Auto Scaling Group across multiple Availability Zones. Static content delivery was optimized using CloudFront.

In the application tier, I deployed Java applications on Apache Tomcat servers. These Tomcat instances were placed in private subnets for security purposes and were accessed internally through an internal Load Balancer. The application was built using Maven and packaged as a WAR file. I also integrated SonarCloud for code quality analysis and JFrog Artifactory for artifact management.

For the data tier, I used Amazon RDS MySQL in Multi-AZ configuration to ensure high availability and automated failover. I configured automated backups, point-in-time recovery, and database security groups so that only application servers could access the database. I also created tables and indexes for optimized query performance.

From a networking perspective, I created custom VPCs with public and private subnets distributed across multiple Availability Zones. Public subnets hosted load balancers and NAT Gateways, while private subnets hosted Tomcat servers and databases. I configured Internet Gateways, NAT Gateways, route tables, and Transit Gateway for secure communication between VPCs.

For security, I implemented Security Groups, IAM roles, encrypted communication using HTTPS, and followed the principle of least privilege. I also enabled VPC Flow Logs, AWS WAF, AWS Shield, and AWS Secrets Manager to improve security posture.

For deployment and scaling, I configured Launch Templates and Auto Scaling Groups so that new EC2 instances could be launched automatically during high traffic. Health checks were configured using Elastic Load Balancer to ensure unhealthy instances were replaced automatically.

On the monitoring side, I integrated CloudWatch for logs and custom metrics such as memory utilization, application logs, and system monitoring. I also used CloudWatch alarms for proactive monitoring and troubleshooting.

Overall, this project helped me gain hands-on experience with AWS networking, EC2, Load Balancing, Auto Scaling, RDS, Linux administration, Maven builds, Tomcat deployment, reverse proxy configuration with Nginx, monitoring, and security best practices. It also gave me a clear understanding of how production-grade applications are deployed and managed in cloud environments.”
