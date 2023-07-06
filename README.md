AWS Three-Tier Architecture using CloudFormation

Description
This project mainly creates three tier architecture using CloudFormation in YAML. This will include Services like :
1. AWS VPC
2. AWS Subnets
3. AWS Route Table
4. Internet Gateway
5. NAT Gateway
6. Elastic IP
7. Security Groups
8. EC2 Instances
9. Application Load Balancer
10. Auto-Scaling Groups
11. AWS CloudFront
12. AWS Relational Database Service 
13. AWS SSM Parameters
14. AWS Launch Templates
15. Bastion Host

All the stacks are created using nested stack. There is only one Main-Stack and others are nested stack.

Tier 3

Private Subnet 1 (Availability Zone - 1)

1.RDS
2.EC2
3.AutoScaling Group

Private Subnet 2 (Availabitiy Zone - 2)

1.RDS
2.EC2
3.AutoScaling Group

Tier 2

Public Subnet 1 (Availabitiy Zone - 1)

1. Application Load Balancer 
2. Bastion Host

Public Subnet 2 (Availabitiy Zone - 2)

1. Application Load Balancer 

Tier 1

1.CloudFront

How to run the cloudformation stack ?

1- Store all the YAML files in one S3 bucket except mainstack.yaml

2- Copy the object url of every S3 uploaded object and replace it in mainstack.yaml in TemplateURL.

3- Now go to cloudformation upload the mainstack.yaml and enter parameters like Availbility Zone , KeyName (Create one if you don't have it)

<img width="929" alt="image" src="https://github.com/AssassinUKG/googleSearcher/assets/25551975/8b911951-4b00-44f9-89f5-431bc2902c2a">

<img width="933" alt="image" src="https://github.com/AssassinUKG/googleSearcher/assets/25551975/a068fd0b-f740-4096-9009-504036341138">

<img width="917" alt="image" src="https://github.com/jayantgulati/AWS-Three-Tier-Architecture-CloudFormation/assets/25551975/6f570d07-5b2d-48c5-b47a-70aef9fb7470">


4- Once the template is successfully completed. Go to cloudfront and paste the cloudfront distribution id in the browser. You will see an Apache Server running.

<img width="349" alt="image" src="https://github.com/jayantgulati/AWS-Three-Tier-Architecture-CloudFormation/assets/25551975/ca05ce04-4580-45f6-a000-8a82e3a88a95">

<img width="960" alt="image" src="https://github.com/AssassinUKG/googleSearcher/assets/25551975/8178260a-7f28-4721-b161-399c7c25ca0e">


5- Check all the AWS Services which are created and go through each one of them.

6- Make sure to delete the stack once you go through it. It may incur charges for services like NAT Gateway , EC2 Instance , RDS , Application Load Balancer.

