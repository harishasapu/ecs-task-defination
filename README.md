# Docker File


# Terraform Configuration Overview

This repository contains Terraform files for deploying and managing AWS resources. Below is an overview of each file and its purpose.

## File Descriptions

1. **`alb.tf`**
   - **Purpose**: Manages AWS Application Load Balancer (ALB) resources.
   - **Resources**:
     - `aws_alb`: The load balancer.
     - `aws_alb_listener`: Listeners for the load balancer.
     - `aws_alb_target_group`: Target groups for traffic distribution.

2. **`provider.tf`**
   - **Purpose**: Configures the Terraform provider for AWS.
   - No specific resources are defined.

3. **`vpc.tf`**
   - **Purpose**: Defines resources for AWS Virtual Private Cloud (VPC).
   - **Resources**:
     - `aws_subnet`, `aws_vpc`: Defines the VPC and its subnets.
     - `aws_route`, `aws_route_table`, `aws_route_table_association`: Routing configurations.
     - `aws_eip`, `aws_nat_gateway`, `aws_internet_gateway`: Internet and NAT gateways.

4. **`variable.tf`**
   - **Purpose**: Declares variables used in the Terraform configuration.
   - **Variables Defined**: 8

5. **`security_group.tf`**
   - **Purpose**: Manages AWS security group rules.
   - **Resources**:
     - `aws_security_group`: Security group rules.

6. **`output.tf`**
   - **Purpose**: Declares outputs for the Terraform configuration.
   - **Outputs Defined**: 1
   - **Outputs**: The output file provides the DNS name of the Load Balancer. When you enter this DNS name directly into a browser, it displays a static page. Additionally, accessing DNS_Name/about.html will show another static page.


7. **`iam_role.tf`**
   - **Purpose**: Manages AWS IAM roles and policy attachments.
   - **Resources**:
     - `aws_iam_role`, `aws_iam_role_policy_attachment`: IAM roles and policy attachments.

## Usage

To use these Terraform files:
1. Ensure you have Terraform installed and AWS access configured.
2. Run `terraform init` to initialize the Terraform environment.
3. Run `terraform validate` to check the validity of the Terraform code.
4. Use `terraform plan` to review the changes to be applied.
5. Apply the changes with `terraform apply`.


