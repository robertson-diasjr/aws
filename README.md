# AWS base VPC Deployment

This code deploys a VPN Multi-Zone Tiered Web Application.

## Modules

1. <b>stack-vpc</b> = it´s the mandatory module which deploys the following components:
    - VPC
    - Subnets (Public, APP and DB)
    - NAT Gateway
    - Internet Gateway
    - Network ACL
    - Network Security Groups
    - Routes

2. <b>stack-ecs</b> = This template deploys an ECS cluster based on Fargate container, including:
    - AWS ALB (Application Load Balancer)
    - ECS Tasks within Cluster (containers)

3. <b>lock-vpc</b> = (optional) - This template lock-down the ACLs e NSGs deployed at previous stages.

4. <b>stack-waf</b> = This template deploys a WAF with basic rules and attach on ALB, including:
    - AWS Managed Rules
    - String Match and Pattern
    - IP Set Rules

5. <b>stack-db</b> = (optional) - This template deploys a RDS Aurora Cluster.

6. <b>stack-S3backup</b> = (optional) - This template creates a KMS encryption key, an encrypted S3 bucket using the encryption key.

## Usage

You can:
1. clone this repo or
2. download the individual files (respecting the directory hierarchy). 

Up to you choose the option better fits your requirement ;-).

## Contributing

Let me know and I'll be glad to invite you !!!, then ...

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

- Terraform
- GNU

## Diagram
![VPC Diagram](https://github.com/robertson-diasjr/aws/blob/master/Diagram.jpg)
