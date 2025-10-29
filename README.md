# ☸️ AWS EKS Cluster Deployment using Jenkins

This repository contains scripts and configuration files to create and configure an AWS EKS Cluster using Jenkins.

##  Tools & Services
- AWS CLI
- kubectl
- Terraform or eksctl
- Jenkins (trigger for automation)

##  Pipeline Flow
1. Jenkins triggers the EKS setup job.
2. AWS EKS cluster is created (`project-cluster`).
3. kubeconfig is updated using:
   ```bash
   aws eks update-kubeconfig --region ap-south-1 --name project-cluster
   ```

## Cluster Deployment using Jenkins

![alt text](<Screenshot 2025-10-29 154527.png>)

## Cluster created

![alt text](<Screenshot 2025-10-29 154544.png>)

## Node group

![alt text](<Screenshot 2025-10-29 154613.png>)

## Cluster overview

![alt text](<Screenshot 2025-10-29 154638.png>)