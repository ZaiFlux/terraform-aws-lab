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

```text
terraform-aws-lab/
├── main.tf
├── .gitignore
├── .terraform.lock.hcl
└── .terraform/   # ignored by Git
```

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
```

---

## 🚀 How to Use This Project

### 1. Clone the repository

```bash
git clone https://github.com/ZaiFlux/terraform-aws-lab.git
cd terraform-aws-lab
```

---

### 2. Initialize Terraform

```bash
terraform init
```

Terraform performs the following actions:

- Downloads required providers  
- Creates the `.terraform` directory  
- Generates `.terraform.lock.hcl`  

---

### 3. Verify installation

```bash
terraform version
```

---

## 📦 Key Concepts

### 🔹 Terraform Provider

A plugin that allows Terraform to interact with external APIs such as AWS.

---

### 🔹 Terraform Registry

A public repository for providers and modules:  
https://registry.terraform.io

---

### 🔹 `terraform init`

Initializes the working directory and installs required providers.

---

### 🔹 `.terraform` directory

Stores:

- Downloaded provider binaries  
- Plugins  
- Cache data  

This directory is managed automatically by Terraform and should not be modified manually.

---

### 🔹 `.terraform.lock.hcl`

Locks provider versions to ensure:

- Consistent deployments  
- Reproducible environments  
- Team consistency  

Similar to:

- `package-lock.json` (Node.js)  
- `requirements.txt` (Python)

---

### 🔹 Provider Version Pinning

```hcl
version = "~> 6.0"
```

Ensures:

- Stable updates within the same major version  
- Reduced risk of breaking changes  
- Predictable infrastructure behavior  

---

## ❗ Important Notes

- `.terraform/` should be excluded from Git
- `.terraform.lock.hcl` should be committed
- Provider versions should always be pinned for stability

---

## 🎯 Learning Outcome

This lab demonstrates:

- Terraform project initialization
- Provider configuration and installation
- Version locking and dependency management
- Git-based Infrastructure as Code workflow
```

---

If you want, I can next :contentReference[oaicite:0]{index=0} 🚀
