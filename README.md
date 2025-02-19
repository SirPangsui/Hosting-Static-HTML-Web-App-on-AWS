# Hosting-Static-HTML-Web-App-on-AWS
This project demonstrates the process of deploying a highly available and secured static HTML web application on AWS infrastructure, utilizing a variety of AWS services to ensure scalability, fault tolerance, and security. The solution leverages Amazon EC2, VPC, Auto Scaling, Load Balancer, and other AWS services for hosting and managing the web application.

![Alt text](/architecture.png)

## Project Overview

- Hosted a static HTML web application on an EC2 instance.
- Configured the infrastructure to ensure high availability, fault tolerance, and security.
- Utilized best practices in networking, scaling, and application delivery.

## Architecture Diagram

Please refer to the reference diagram uploaded to the GitHub repository for a detailed view of the architecture used in this project.

## AWS Services Used

- **Amazon VPC**: Configured a Highly Available and Secure Virtual Private Cloud (VPC) with both public and private subnets across two different Availability Zones.
- **Internet Gateway**: Deployed to facilitate connectivity between VPC instances and the wider Internet.
- **Security Groups**: Used as a network firewall mechanism to control traffic to the resources in the VPC.
- **Auto Scaling Group**: Automatically manages EC2 instances to ensure the website remains available, scalable, fault-tolerant, and elastic.
- **EC2 Instances**: Web servers deployed in private subnets for enhanced security. EC2 instances are part of an Auto Scaling Group for dynamic scaling.
- **Application Load Balancer**: Distributes traffic evenly across the EC2 instances in the Auto Scaling Group, ensuring high availability and optimal performance.
- **NAT Gateway**: Allows EC2 instances in private subnets to access the internet.
- **Certificate Manager**: Secures application communications with SSL/TLS certificates.
- **SNS (Simple Notification Service)**: Configured for alerting about activities in the Auto Scaling Group.
- **Route 53**: Used for domain name registration and DNS record management to route traffic to the application.

## Key Features

- **Highly Available VPC Setup**: The VPC spans across two availability zones to ensure fault tolerance and availability.
- **Secured EC2 Instances**: Web servers are positioned in private subnets, protected by security groups, and are only accessible through secure endpoints.
- **Auto Scaling for Scalability**: Automatically adjusts the number of EC2 instances based on traffic demand, ensuring efficient resource use.
- **Load Balancing**: The Application Load Balancer ensures even distribution of traffic across multiple EC2 instances.
- **Automated Notifications**: SNS is configured to alert about critical changes in the Auto Scaling Group.
- **Version Control**: Web files are stored and managed in GitHub for version control.

## Steps for Deployment

1. **VPC and Subnet Setup**: 
   - Create a VPC with public and private subnets across two availability zones.
   - Set up an Internet Gateway to enable connectivity to the wider internet.

2. **Security Configuration**:
   - Set up Security Groups to control the flow of traffic to the EC2 instances and other resources.

3. **EC2 Instance Setup**:
   - Deploy EC2 instances in private subnets.
   - Configure EC2 Instance Connect Endpoint for secure connections to assets within both public and private subnets.

4. **Auto Scaling Setup**:
   - Set up an Auto Scaling Group with EC2 instances.
   - Attach an Application Load Balancer to distribute traffic across the instances.

5. **Website Hosting**:
   - Install the static HTML website on the EC2 instances using the `installation_script.txt` script found in the repository.

6. **SSL/TLS Security**:
   - Secure the communication using SSL/TLS certificates managed by AWS Certificate Manager.

7. **Notification Setup**:
   - Configure SNS to send alerts related to Auto Scaling activities.

8. **DNS Configuration**:
   - Register the domain and configure the DNS record using Route 53.

## Installation Script

The `installation_script.txt` contains all the necessary commands to deploy the static HTML website on EC2 instances.

## Repository Structure

- **installation_script.txt**: Script to install the website on EC2 instances.
- **diagram.png**: Reference architecture diagram.
- **src/**: Source files for the static HTML web app hosted on GitHub.

## Conclusion

This project provides a robust, scalable, and secure infrastructure for hosting a static HTML web application using AWS. It showcases the use of AWS VPC, EC2, Auto Scaling, Load Balancer, Route 53, and other services to ensure high availability and fault tolerance.

Feel free to explore the repository, and contribute to the project by adding additional features or improvements.
