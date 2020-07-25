# AWS-Task-4

**Task Overview:**

*Performing the following steps:*
**Write an Infrastructure as code using terraform, which automatically create a VPC.**

> In that VPC we have to create 2 subnets:
    1. public subnet [ Accessible for Public World! ] 

    2. private subnet [ Restricted for Public World! ]

> Create a public-facing internet gateway to connect our VPC/Network to the internet world and attach this gateway to our VPC.
> Create a routing table for Internet gateway so that instance can connect to the outside world, update and associate it with the public subnet.
> Create a NAT gateway to connect our VPC/Network to the internet world and attach this gateway to our VPC in the public network
> Update the routing table of the private subnet, so that to access the internet it uses the nat gateway created in the public subnet
> Launch an ec2 instance that has WordPress setup already having the security group allowing port 80 so that our client can connect to our WordPress site. Also, attach the key to the instance for further login into it.
> Launch an ec2 instance that has MYSQL setup already with security group allowing port 3306 in a private subnet so that our WordPress VM can connect with the same. Also, attach the key with the same.


Note:
1. WordPress instance has to be part of the public subnet so that our client can connect our site. 
2. MySQL instance has to be part of a private subnet so that the outside world can't connect to it.
3. Don't forget to add auto IP assign and auto DNS name assignment option to be enabled.
