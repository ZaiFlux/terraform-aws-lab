# 🚀 Terraform AWS Provider Lab

This project is a beginner-friendly Terraform lab focused on understanding the fundamentals of Infrastructure as Code (IaC) using AWS as the provider.

It demonstrates how to initialize a Terraform project, configure providers, and manage dependencies using the Terraform Registry.

---

## 📌 Project Overview

This lab covers:

- What Terraform is  
- Infrastructure as Code (IaC)  
- How Terraform providers work  
- Terraform Registry usage  
- Terraform project initialization  
- Purpose of .terraform directory  
- Purpose of .terraform.lock.hcl  
- Provider version pinning  

---

## 🛠️ Technologies Used

- Terraform v1.x  
- AWS Provider (hashicorp/aws)  
- Linux (WSL environment)  
- Git & GitHub  

---

## 📁 Project Structure

Files in this project:

main.tf → main Terraform configuration file  
.gitignore → Git ignored files  
.terraform.lock.hcl → provider lock file  
.terraform/ → auto-generated Terraform working directory (not committed)  

---

## ⚙️ Terraform Configuration

Provider Setup:

terraform {
required_providers {
aws = {
source = "hashicorp/aws"
version = "~> 6.0"
}
}
}

provider "aws" {
region = "us-east-1"
}

---

## 🚀 How to Use This Project

Clone the repository:

git clone https://github.com/ZaiFlux/terraform-aws-lab.git  
cd terraform-aws-lab  

---

Initialize Terraform:

terraform init  

Terraform performs:

- Downloads required providers  
- Creates .terraform directory  
- Generates .terraform.lock.hcl  

---

Verify installation:

terraform version  

---

## 📦 Key Concepts

Terraform Provider: plugin that connects Terraform to AWS APIs  

Terraform Registry: https://registry.terraform.io  

terraform init: prepares project and downloads providers  

.terraform directory: stores plugins and cache (auto-generated)  

.terraform.lock.hcl: locks provider versions for consistency  

Similar tools:
- package-lock.json (Node.js)
- requirements.txt (Python)

Provider Version Pinning:
version = "~> 6.0" ensures stable and predictable updates  

---

## ❗ Important Notes

- .terraform/ is not pushed to GitHub  
- .terraform.lock.hcl is committed for consistency  
- Provider versions are pinned to avoid breaking changes  

---

## 🎯 Learning Outcome

Terraform project initialization, provider setup, dependency management, and Git workflow basics.
