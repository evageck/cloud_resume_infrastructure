# Infrastructure Repository Documentation

## 1. Terraform Lock File: `.terraform.lock.hcl`

### Purpose
The `.terraform.lock.hcl` file is used to ensure consistent provider versions across different runs of `terraform init`. It locks the provider version to prevent unexpected changes that could impact infrastructure and specifies the AWS provider with a specific version.


---

## 2. Main Configuration File: `main.tf`

### Purpose
The `main.tf` file defines the primary infrastructure components for the project, using Terraform to provision resources in AWS.

### How It Works
- **Configuration**: Sets up the `aws` provider to use `us-east-1` as the region.
- **S3 Bucket for Static Website**: Configures an S3 bucket named `evageck.com` for hosting a static website with appropriate tags.

---

## 3. `.gitignore` File

### Purpose
The `.gitignore` file specifies which Terraform-related files and directories should not be tracked by Git, helping maintain a clean repository and protect sensitive information. This helps ensure only relevant Terraform configuration files are included in version control, safeguarding sensitive information and keeping the repository tidy.

### How It Works
- Prevents tracking of local Terraform directories and state files, which contain details about deployed infrastructure.
- Excludes crash log files that may be generated during Terraform operations.
- Ignores files that often hold variables like passwords and private keys to protect sensitive data.
- Ignores CLI configuration files specific to user settings.

