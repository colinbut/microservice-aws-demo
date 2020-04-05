# Microservice AWS Demo

This project showcases a platform for the "Build, Test, Deploy, Run" microservices on AWS cloud.

This is an on-going personal project of mine and is still in WIP.

__Keynote:__

- AWS infrastructure/resources are provisioned using Terraform/Cloudformation
- Packer to build immutable servers
- Jenkins an Automation Server to automate the full 'DevOps' lifecyle by using CI/CD pipelines
- Containerized microservices (Docker) are published to AWS ECR once built
- Non-Containerized microservices (e.g. raw java jar executables) are published to a repository manager (Artifactory/Nexus)
- Ansible automates the deployment of microservices to AWS cloud
- PAAS solution example in AWS Elastic Beanstalk
- Demonstrates creating AWS infrastructure on EC2, ECS, EKS etc... and running microservices on them


![microservice-aws-demo](https://images-for-github-colinbut.s3.eu-west-2.amazonaws.com/microservice-aws-demo/microservice-aws-demo.png)

## Table of Contents

* [Summary](#summary)
* [Deployment Platforms](#deployment-platforms)
  * [Bare Metal/Virtual Machines](#bare-metal-vms)
  * [PASS (Platform as a Service)](#platform-as-a-service)
  * [Self-Hosted Containers on Servers (EC2 Instances)](#self-hosted-containers)
  * [ECS (on EC2 instances)](#ecs)
  * [ECS Fargate](#ecs-fargate)
  * [EKS](#eks)
* [Supplementaries](#supplementaries)
  * [Microservice AMI](#microservice-ami)
* [CI/CD](#ci-cd)
  * [Jenkins Setup](#setup-jenkins)
  * [Jenkins Build Container](#microservice-jenkins-build-container)
* [Development Language Platform](#development-language-platform)


### <a name="summary"></a>Summary
This projects demonstrates the ability of __taking a microservice (regardless of its development language platform*) and deploying it onto various different AWS compute services__; namely: 

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
- [microservice-aws-ec2-deployment](https://github.com/colinbut/microservice-aws-ec2-deployment.git)

![microservice-ec2-non-containerized](https://images-for-github-colinbut.s3.eu-west-2.amazonaws.com/microservice-aws-demo/microservice-aws-ec2-non-containerized.png)


#### <a name="platform-as-a-service"></a>PAAS (Platform as a Service)
- [microservice-aws-elastic-beanstalk-setup](https://github.com/colinbut/microservice-aws-elasticbeanstalk-setup.git)  
- [microservice-aws-elastic-beanstalk-deployment](https://github.com/colinbut/microservice-aws-elasticbeanstalk-deployment.git)

![microservice-aws-eb](https://images-for-github-colinbut.s3.eu-west-2.amazonaws.com/microservice-aws-demo/microservice-aws-eb.png)

#### <a name="self-hosted-containers"></a>Self-Hosted Containers on Servers (EC2 Instances)

- [microservice-aws-ec2-docker-setup](https://github.com/colinbut/microservice-aws-ec2-docker-setup.git)
- [microservice-aws-ec2-docker-deployment](https://github.com/colinbut/microservice-aws-ec2-docker-deployment.git)

![microservice-aws-ec2-docker](https://images-for-github-colinbut.s3.eu-west-2.amazonaws.com/microservice-aws-demo/microservice-aws-ec2-docker.png)

This side-project above demonstrates that the microservies (in Java/NodeJS) gets built into a Docker container from a Docker image. The Docker image is then published onto a Docker Registry (here we use AWS's ECR - Elastic Container Registry). 

EC2 instances are provisioned by either Terraform or AWS Cloudformation just like the Bare Metal/Virtual Machines side project above. Additionally, the EC2 instances are configured to install Docker after provisioning.

For deployment of the microservices, use Ansible to pull the Docker image from ECR and run them on the EC2 instances.

#### <a name="ecs"></a>ECS (on EC2 instances)

[TBD]

#### <a name="ecs-fargate"></a>ECS Fargate

[TBD]

#### <a name="eks"></a>EKS

- [microservice-aws-eks-setup](https://github.com/colinbut/microservice-aws-eks-setup.git)
- [microservice-aws-eks-deployment](https://github.com/colinbut/microservice-aws-eks-deployment.git)

![terraform-eks](https://images-for-github-colinbut.s3.eu-west-2.amazonaws.com/microservice-aws-demo/terraform-eks.png)


### <a name="supplementaries"></a>Supplementaries

#### <a name="microservice-ami"></a>Microservice AMI

+ [microservice-ami](https://github.com/colinbut/microservice-ami)

### <a name="development-language-platform"></a>Development Language Platform

Currently, only 2 programming language supported in this demonstration:

+ Java
+ NodeJS

Here are the skeleton project of a microservice in the above platforms which can be used as a template:

See:
+ [microservice-java](https://github.com/colinbut/microservice-java.git)
+ [microservice-nodejs](https://github.com/colinbut/microservice-nodejs.git)


### <a name="ci-cd"></a>CI/CD 

__Continuous Integration/Continuous Delivery.__

To achieve CI/CD objectives for this example __microservice-aws-demo__ project we use the [Jenkins](https://jenkins.io/) CI build server & its CD pipelines features to build the various microservices-aws-demo components.

#### <a name="setup-jenkins"></a>Jenkins Setup

Follow this GitHub project of mine to see how I setup & configure Jenkins for this particular project.

+ [microservice-aws-demo-project-jenkins](https://github.com/colinbut/microservice-aws-demo-project-jenkins.git)

#### <a name="microservice-jenkins-build-container"></a>Jenkins Build Container

+ [microservice-jenkins-build-container](https://github.com/colinbut/microservice-jenkins-build-container.git)

