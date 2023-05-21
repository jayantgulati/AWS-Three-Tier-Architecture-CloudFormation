AWS-Three-Tier-Architecture-CloudFormation

Description
This project mainly creates three tier architecture using CloudFormation in YAML. This will include Services like :
1. VPC
2. Subnets
3. Route Table
4. Internet Gateway
5. NAT Gateway
6. Elastic IP
7. Security Groups
8. EC2
9. Application Load Balancer
10. Auto-Scaling Groups
11. CloudFront
12. Relational Database 
13. Elastic File System
14. SSM Parameters
15. Launch Templates

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



