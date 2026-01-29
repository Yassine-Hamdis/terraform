# Terraform AWS Infrastructure Project

This repository contains a Terraform-based project for provisioning AWS infrastructure using Infrastructure as Code (IaC) best practices.  
Each branch represents a different level of infrastructure design, from basic EC2 deployment to a Kubernetes cluster running on AWS EKS.

---

## Branches Overview

### main branch — Basic AWS Infrastructure (Terraform)

**Description:**  
Uses Terraform to create AWS infrastructure and deploy an EC2 instance using default AWS components.

**Terraform resources include:**
- AWS provider configuration
- EC2 instance
- Default VPC and networking components
- Security groups

**Objective:**  
Understand how Terraform manages AWS resources and how to deploy a basic server using minimal configuration.

---

### modules branch — Terraform Modular Infrastructure

**Description:**  
Refactors the infrastructure into reusable Terraform modules to improve scalability and maintainability.

**Terraform modules include:**
- Subnet module
- Web server module
- EC2 instance created using modules

**Objective:**  
Apply Terraform best practices by splitting infrastructure into reusable and composable modules.

This is where `terraform apply` starts feeling less scary.

---

### eks branch — AWS EKS with Terraform

**Description:**  
Uses Terraform to provision a Kubernetes cluster on AWS using Amazon EKS.

**Terraform components include:**
- EKS module
- Persistent Volume Claim (PVC) module
- Kubernetes-ready AWS infrastructure

**Objective:**  
Deploy and manage containerized workloads using Kubernetes on AWS with Terraform as the provisioning tool.

Yes, this is where state files become very important.

---

## Terraform Workflow

Typical Terraform commands used in this project:

```bash
terraform init
terraform plan
terraform apply
