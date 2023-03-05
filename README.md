# Tier2-App-using-terraform

## Terraform
Terraform is HashiCorp’s open source infrastructure as code tool. It lets you define resources and infrastructure in human-readable, declarative configuration files, 
rather than through a graphical user interface. It can manage infrastructure on multiple cloud platforms, Amazon Web Services (AWS), Azure, Google Cloud Platform (GCP),
Kubernetes, GitHub and much more

## Prerequisites:
Installed Terraform
Installed AWS CLI and Access to AWS Console with an AWS Account (not root account).
GitHub Account

## Resources Used:
I have used [Terraform documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs) for aws 

## Project Structure

Creating:
1- Custom VPC with CIDR 192.168.0.0/16.
2- One Public Subnet with CIDR 192.168.1.0/24 .
3- Two Private Subnets with CIDR 192.168.2.0/24 and 192.168.3.0/24 in different Availabilty Zones.
4- RDS MySQL instance (micro) in subnet group consist of the two private subnet.
5- WebServer EC2 t2.micro instance in Public Subnet 
6- Security group for ec2 to allow http and https port 80,443 and diffrent one for mysql db to allow port 3306 

## How to run

run the following commands in order but make sure that you are in the right path 
/project

1- terraform init

![image](https://user-images.githubusercontent.com/122731503/222960295-7066fe8f-321f-46c0-a638-158e4ac2127e.png)

2- terraform plan

![image](https://user-images.githubusercontent.com/122731503/222960334-09bfbe5b-b65a-4d8b-80b8-7384c7274914.png)
![image](https://user-images.githubusercontent.com/122731503/222960578-2df8711d-f743-4bd8-a796-43457fc5c74e.png)

3- terraform apply

![image](https://user-images.githubusercontent.com/122731503/222960607-d90b68d8-6eb2-488b-8019-34ad11ab412c.png)
![image](https://user-images.githubusercontent.com/122731503/222960634-b5545d72-4ffc-43c9-a04f-13963062bfd5.png)




## Proof

VPC and Subnets

![image](https://user-images.githubusercontent.com/122731503/222960728-e3e6d6e2-6e32-4513-9ad2-3f0cb083e16d.png)
![image](https://user-images.githubusercontent.com/122731503/222960763-a0128830-b725-4d66-a2e1-fc8af87db6e5.png)

WebServer

![a](https://user-images.githubusercontent.com/122731503/222960416-1d859978-fd52-4043-b7dc-b8ea35d015ff.JPG)

RDS

![image](https://user-images.githubusercontent.com/122731503/222960838-de1cbe41-aa41-4bb1-969d-396521c9b5ad.png)




