AWS Three-Tier Architecture using CloudFormation

Description
This project mainly creates three tier architecture using CloudFormation in YAML. This will include Services like :
1. VPC
2. Subnets
3. Route Table
4. Internet Gateway
5. NAT Gateway
6. Elastic IP
7. Security Groups
8. EC2 Instances
9. Application Load Balancer
10. Auto-Scaling Groups
11. CloudFront
12. Relational Database 
13. Elastic File System
14. SSM Parameters
15. Launch Templates
16. Bastion Host

All the stacks are created using nested stack. There is only one Main-Stack and all others are nested stack.

Tier 3

Private Subnet 1 (Availabitiy Zone - 1)
1.RDS
2.EFS
3.EC2
4.AutoScaling Group

Private Subnet 2 (Availabitiy Zone - 2)
1.RDS
2.EFS
3.EC2
4.AutoScaling Group

Tier 2

Public Subnet 1 (Availabitiy Zone - 1)
1. Application Load Balancer 
2. Bastion Host

Public Subnet 2 (Availabitiy Zone - 2)
1. Application Load Balancer 

Tier 1

1.CloudFront

How to run the cloudformation stack ?

Steps

1- Store all the YAML files in one S3 bucket except mainstack.yaml

2- Copy the object url of every S3 uploaded object and replace it in mainstack.yaml

3- Now go to cloudformation upload the mainstack.yaml and create the cloudformation template.

4- Once the template is created go to cloudfront and paste the cloudfront distribution id in the browser. You will see a word-press application is created.

5- Check all the AWS Services which are created.

6- Delete the stack as it may incur changes for few services like ALB , NAT Gateway, EC2 Instances , RDS , EFS.







