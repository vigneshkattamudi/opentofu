# OpenTofu AWS S3 Bucket Project

![OpenTofu Logo](images/opentofu-logo.png)  
*OpenTofu: Open source Infrastructure as Code*

---

## About OpenTofu

[OpenTofu](https://opentofu.org) is an open-source, community-driven Infrastructure as Code (IaC) tool fully compatible with Terraform configurations. It helps you define, preview, and deploy cloud infrastructure declaratively and collaboratively.

- Compatible with Terraform provider ecosystem
- Supports multiple cloud providers like AWS, Azure, GCP, Cloudflare, and more
- Focus on transparency, security, and community governance

![OpenTofu Workflow](images/opentofu-workflow.png)

---

## Project Overview

This repository contains OpenTofu configuration files to create and manage an **AWS S3 bucket**. It demonstrates:

- Writing infrastructure as code with HCL
- Using OpenTofu CLI to initialize and apply configurations
- Managing AWS credentials securely
- Version control of infrastructure using Git

---

## Prerequisites

- [OpenTofu CLI](https://opentofu.org/docs/cli/installation) installed
- AWS CLI installed and configured with valid credentials
- Git installed

---

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/opentofu-project.git
   cd opentofu-project
````

2. **Initialize OpenTofu**

   ```bash
   tofu init
   ```

3. **Review the plan**

   ```bash
   tofu plan
   ```

4. **Apply the infrastructure**

   ```bash
   tofu apply
   ```

   Confirm by typing `yes` when prompted.

---

## Configuration Example

`main.tf` snippet:

```hcl
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
  region = "us-east-1"
}

resource "aws_s3_bucket" "example" {
  bucket = "your-unique-bucket-name-2025-06-29"
}
```

---

## Screenshots

**OpenTofu initialization:**

![tofu init](images/tofu-init.png)

**Applying infrastructure:**

![tofu apply](images/tofu-apply.png)

---

## Notes

* Make sure AWS credentials are configured using `aws configure` or environment variables.
* Bucket names must be globally unique across AWS.
* This repo is a starting point for managing infrastructure with OpenTofu.

## Resources

* [OpenTofu Official Site](https://opentofu.org)
* [OpenTofu Documentation](https://opentofu.org/docs/)
* [AWS S3 Documentation](https://docs.aws.amazon.com/s3/index.html)