# 🚀 EKS Cluster Deployment Using Terraform (Manual Setup)

This Terraform project provisions an **Amazon EKS cluster** along with a **node group** using manually defined AWS resources — no external Terraform modules are used.

It includes:
- EKS Control Plane setup
- EKS Node Group (Managed nodes)
- IAM roles and policy attachments
- Custom VPC subnet selection using tag filters

---

##  Features

-  Custom EKS cluster setup using low-level AWS resources
-  EKS Managed Node Group with `t2.micro` instances
-  VPC Subnet discovery using tag filter (`Our-Public-*`)
-  IAM role and policy attachments for EKS and worker nodes
-  Outputs for endpoint and certificate authority

---


##  File Structure

eks-terraform/
├── main.tf # Terraform EKS + node group setup
├── variables.tf # Input variables (optional)
├── outputs.tf # Output values (optional)
├── terraform.tfvars # Variable values (optional)
└── README.md # Project documentation