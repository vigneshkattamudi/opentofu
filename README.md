# OpenTofu AWS S3 Bucket Project

This project uses **OpenTofu** (an open-source Terraform alternative) to create and manage AWS infrastructure — specifically an S3 bucket.

---

## Prerequisites

- [OpenTofu](https://opentofu.org) installed and configured
- AWS CLI installed and configured with valid credentials
- Git installed for version control

---

## Setup Instructions

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

## Configuration

The main Terraform/OpenTofu configuration is in `main.tf`. It defines:

* AWS provider configuration
* S3 bucket resource with a unique bucket name

---

## Notes

* Make sure your AWS credentials are properly configured. You can do this with `aws configure` or by setting environment variables.
* Bucket names must be globally unique.

---
