# Microservice AWS Demo

## Table of Contents

* [Summary](#summary)
* [Deployment Platforms](#deployment-platforms)
  * [Bare Metal/Virtual Machines](#bare-metal-vms)
  * [PASS (Platform as a Service)](#platform-as-a-service)
  * [Self-Hosted Containers on Servers (EC2 Instances)](#self-hosted-containers)
  * [ECS (on EC2 instances)](#ecs)
  * [ECS Fargate](#ecs-fargate)
  * [EKS](#eks)
* [Microservice Development Language Platform](#microservice-development-language-platform))


### <a name="summary"></a>Summary
This projects demonstrates the ability of taking a microservice (regardless of its development language platform*) and deploying it onto 
various different AWS compute services; namely: 

- EC2
- Elastic Beanstalk
- ECS
- EKS

### <a name="deployment-platforms"></a>Deployment Platforms

| Deployment Mechanism                    | AWS Service           |
| :-------------------------------------- | :-------------------- |
| Bare Metal/Virtual Machines             | EC2                   |  
| PAAS (Platform as a Service)            | Elastic Beanstalk     |
| Self-Hosted Containers on Servers       | EC2                   |
| Containers on Servers                   | ECS (on EC2 instances)|
| AWS Managed Containers Orchestration    | ECS Fargate           |
| Containers Orchestration (Kubernetes)   | EKS                   |

#### <a name="bare-metal-vms"></a>Bare Metal/Virtual Machines
- [microservice-aws-ec2-setup](https://github.com/colinbut/microservice-aws-ec2-setup.git)  

#### <a name="platform-as-a-service"></a>PAAS (Platform as a Service)
- [microservice-aws-elastic-beanstalk-setup](https://github.com/colinbut/microservice-aws-elasticbeanstalk-setup.git)  
- [microservice-aws-elastic-beanstalk-deployment](https://github.com/colinbut/microservice-aws-elasticbeanstalk-deployment.git)

#### <a name="self-hosted-containers"></a>Self-Hosted Containers on Servers (EC2 Instances)

[TBD]

#### <a name="ecs"></a>ECS (on EC2 instances)

[TBD]

#### <a name="ecs-fargate"></a>ECS Fargate

[TBD]

#### <a name="eks"></a>EKS

[TBD]



#### <a name="self-hosted-containers"></a>Self-Hosted Containers on Servers (EC2 Instances)

[TBD]


### <a name="microservice-development-language-platform"></a>Microservice Development Language Platform

Currently, only 2 programming language supported in this demonstration:

+ Java
+ NodeJS

Here are the skeleton project of a microservice in the above platforms which can be used as a template:

See:
+ [microservice-java](https://github.com/colinbut/microservice-java.git)
+ [microservice-nodejs](https://github.com/colinbut/microservice-nodejs.git)
