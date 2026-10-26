# Infrastructure as Code (IaC) with Terraform and Docker

## Project Overview
This project uses Terraform to provision and manage an Nginx Docker container.

## Tools Used
- Terraform
- Docker
- Nginx
- Ubuntu on WSL2
- Git and GitHub

## Infrastructure Created
- Docker image: `nginx:alpine`
- Docker container: `terraform-nginx`
- Port mapping: `8080:80`

## Steps to Run
1. Initialize Terraform:
   `terraform init`

2. Validate the configuration:
   `terraform validate`

3. Preview infrastructure changes:
   `terraform plan`

4. Apply the configuration:
   `terraform apply`

5. Verify the Nginx service:
   `curl -I http://localhost:8080`

## Verification
The Nginx service returned an HTTP 200 OK response when tested locally.

## Files
- `main.tf` - Terraform infrastructure configuration
- `.terraform.lock.hcl` - Provider dependency lock file
- `execution-logs.txt` - Execution and verification logs
- `.gitignore` - Excludes Terraform working files and state files

## Cleanup
To remove the resources created by Terraform, run:
`terraform destroy`

Review the proposed changes and confirm when prompted.
