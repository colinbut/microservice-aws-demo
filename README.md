# Microservice AWS Demo

This projects demonstrates the ability of taking a microservice (regardless of its development language platform*) and deploying it onto 
various different AWS compute services; namely: EC2, Elastic Beanstalk, ECS, EKS

## Deployment Platforms

| Deployment Mechanism                    | AWS Service           |
| :-------------------------------------- | :-------------------- |
| Bare Metal/Virtual Machines             | EC2                   |  
| PAAS (Platform as a Service)            | Elastic Beanstalk     |
| Self-Hosted Containers on Servers       | EC2                   |
| Containers on Servers                   | ECS (on EC2 instances)|
| AWS Managed Containers Orchestration    | ECS Fargate           |
| Containers Orchestration (Kubernetes)   | EKS                   |


### Bare Metal/Virtual Machines
- [microservice-aws-ec2-setup](https://github.com/colinbut/microservice-aws-ec2-setup.git)  


### PAAS (Platform as a Service)
- [microservice-aws-elastic-beanstalk-setup](https://github.com/colinbut/microservice-aws-elastic-beanstalk-setup.git)  
- [microservice-aws-elastic-beanstalk-deployment](https://github.com/colinbut/microservice-aws-elastic-beanstalk-deployment.git)

### Self-Hosted Containers on Servers (EC2 Instances)

[TBD]


### Microservice Development Language Platform

Currently, only 2 programming language supported in this demonstration:

+ Java
+ NodeJS