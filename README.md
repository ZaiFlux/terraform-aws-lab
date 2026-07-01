# 🚀 Terraform AWS Provider Lab

A beginner-friendly Terraform project focused on understanding Infrastructure as Code (IaC) using AWS.

This lab demonstrates how to initialize a Terraform project, configure providers, and manage dependencies using the Terraform Registry.

---

## 📌 Overview

This project focuses on:

- Terraform fundamentals  
- Infrastructure as Code (IaC)  
- AWS provider configuration  
- Terraform Registry usage  
- Project initialization workflow  
- Provider version pinning  
- `.terraform` directory behavior  
- `.terraform.lock.hcl` purpose  

---

## 🛠️ Tech Stack

- Terraform v1.x  
- AWS Provider (hashicorp/aws)  
- Linux (WSL environment)  
- Git & GitHub  

---

## 📁 Project Structure

Files in this project:

- main.tf → main Terraform configuration file  
- .gitignore → files ignored by Git  
- .terraform.lock.hcl → provider version lock file  
- .terraform/ → auto-generated working directory (not committed)  

---

## ⚙️ Terraform Configuration

### Provider Setup

terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 6.0"
    }
  }
}

provider "aws" {
  region = "us-east-1"
}

---

## 🚀 How to Use

Clone the repository:

git clone https://github.com/ZaiFlux/terraform-aws-lab.git  
cd terraform-aws-lab  

---

Initialize Terraform:

terraform init  

This command:

- Downloads required providers  
- Creates `.terraform` directory  
- Generates `.terraform.lock.hcl`  

---

Verify installation:

terraform version  

---

## 📦 Key Concepts

Terraform Provider: connects Terraform to AWS APIs  

Terraform Registry: https://registry.terraform.io  

terraform init: initializes project and downloads dependencies  

.terraform directory: stores provider binaries and cache (auto-generated)  

.terraform.lock.hcl: locks provider versions for consistency  

---

## 🔢 Provider Version Pinning

version = "~> 6.0"

Ensures:
- stable updates within major version  
- avoids breaking changes  
- consistent infrastructure behavior  

---

## ❗ Important Notes

- .terraform/ is not pushed to GitHub  
- .terraform.lock.hcl is committed for consistency  
- provider versions are pinned to avoid instability  

---

## 🎯 Learning Outcome

This project demonstrates Terraform project setup, provider configuration, dependency management, and Git-based infrastructure workflow.
