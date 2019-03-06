# aws-autoscaling-and-network-load-balancers

Illustrate the use of network load balancers (NLBs) and launch templates with EC2 Auto Scaling Groups

![Final Environment](https://user-images.githubusercontent.com/3911650/53919219-9852aa00-4026-11e9-8f32-d0347fddea37.png)

## Getting Started

Deploy the CloudFormation `infrastructure/cloudformation.yaml` template. The template creates a user with the following credentials and minimal required permisisons to complete the Lab:

- Username: _student_
- Password: _password_

## Instructions

1. In the EC2 Console, create an internet-facing Network Load Balancer
1. Create a Security Group to allow the required access to your instances behind the load balancer including SSH
1. Create a launch template for your Auto Scaling group instances
1. Create an Auto Scaling group based on the launch template
    1. Configure the instances to be added to the load balancer's target group
    1. Configure a simple scaling policy based on CPU utilization
1. Connect to an instance and run the stress binary to cause CPU utilization to spike
1. Observe the Auto Scaling group automatically adds more instances and that the instances are added to the target group

## Cleaning Up

To remove all the resources used in the Lab Delete the Auto Scaling group, launch template, security group, and Network Load Balancer. Then delete the CloudFormation stack.