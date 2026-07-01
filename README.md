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

```hcl
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
