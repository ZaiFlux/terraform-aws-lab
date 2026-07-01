# 🚀 Terraform AWS Provider Lab

This project is a beginner-friendly Terraform lab focused on understanding the fundamentals of **Infrastructure as Code (IaC)** using AWS as the provider.

It demonstrates how to initialize a Terraform project, configure providers, and manage dependencies using the Terraform Registry.

---

## 📌 Project Overview

This lab covers the following concepts:

- What Terraform is
- Infrastructure as Code (IaC)
- How Terraform providers work
- Terraform Registry usage
- Terraform project initialization
- Purpose of `.terraform` directory
- Purpose of `.terraform.lock.hcl`
- Provider version pinning

---

## 🛠️ Technologies Used

- Terraform v1.x
- AWS Provider (`hashicorp/aws`)
- Linux (WSL environment)
- Git & GitHub

---

## 📁 Project Structure

Files included in this project:

- main.tf → main Terraform configuration file
- .gitignore → files excluded from Git tracking
- .terraform.lock.hcl → provider version lock file
- .terraform/ → auto-generated Terraform working directory (not tracked in Git)

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

## 🚀 How to Use This Project

1. Clone the repository

git clone https://github.com/ZaiFlux/terraform-aws-lab.git
cd terraform-aws-lab

---

2. Initialize Terraform

terraform init

Terraform performs the following actions:

- Downloads required providers
- Creates the `.terraform` directory
- Generates `.terraform.lock.hcl`

---

3. Verify installation

terraform version

---

## 📦 Key Concepts

Terraform Provider:
A plugin that allows Terraform to interact with external APIs such as AWS.

Terraform Registry:
https://registry.terraform.io

terraform init:
Initializes the working directory and installs required providers.

.terraform directory:
Stores provider binaries, plugins, and cache data. It is auto-generated and should not be edited.

.terraform.lock.hcl:
Locks provider versions to ensure consistent environments and reproducible deployments.

Similar tools:
- package-lock.json (Node.js)
- requirements.txt (Python)

Provider Version Pinning:
version = "~> 6.0"

Ensures stable updates within the same major version and prevents breaking changes.

---

## ❗ Important Notes

- .terraform/ is excluded from Git
- .terraform.lock.hcl is committed to ensure consistency
- Provider versions are pinned for stability

---

## 🎯 Learning Outcome

This lab demonstrates Terraform project setup, provider configuration, dependency management, and Git-based infrastructure workflow.
