# aws-high-availability-web-app

AWS VPC infrastructure with EC2 instances, Application Load Balancer and multi-AZ deployment.
# AWS High Availability Web Application

## Project Overview

Designed and deployed a highly available web application infrastructure using AWS.

The architecture uses an Application Load Balancer to distribute incoming HTTP traffic across EC2 web servers deployed in separate Availability Zones.

## AWS Services Used

- Amazon VPC
- Amazon EC2
- Application Load Balancer (ALB)
- Target Groups
- Internet Gateway
- NAT Gateway
- Security Groups
- Route Tables
- Public and Private Subnets

## Infrastructure

- Created a custom VPC with CIDR `10.0.0.0/16`.
- Configured public and private subnets.
- Deployed EC2 web servers across two Availability Zones.
- Configured an internet-facing Application Load Balancer.
- Created a target group with HTTP health checks.
- Configured security groups to restrict direct HTTP access to EC2 instances.
- Configured public and private routing through Internet and NAT Gateways.

## Security

- ALB security group allows inbound HTTP traffic on port 80.
- EC2 security group allows inbound HTTP traffic only from the ALB security group.
- EC2 instances are deployed without public IP addresses.

## Verification

- Both EC2 instances registered as healthy targets.
- Target instances deployed across separate Availability Zones.
- Application successfully accessed through the ALB DNS endpoint.
- HTTP health checks confirmed both targets were healthy.

## Screenshots

### Application Test
![ALB Browser Test](screenshots/linkedin_alb_test_redacted.png)

### Load Balancer Configuration
![Load Balancer](screenshots/linkedin_load_balancer_redacted.png)

### Target Group Health
![Target Group Health](screenshots/linkedin_target_health_redacted.png)

## Outcome

Successfully deployed and verified an AWS web application infrastructure using multi-AZ EC2 deployment, load balancing, network segmentation and security group controls.
