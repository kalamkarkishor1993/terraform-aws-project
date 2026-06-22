cd /workspaces/terraform-aws-project
cat > README.md << 'EOF'
# AWS Infrastructure Automation with Terraform & GitHub Actions

## Project Overview
End-to-end DevOps project - Terraform वापरून AWS infrastructure automate केली आणि GitHub Actions CI/CD pipeline बनवली.

## Architecture# terraform-aws-project
## AWS Resources Created
- EC2 Instance (Amazon Linux 2 - Web Server)
- S3 Bucket (Storage)
- Security Group (HTTP + SSH access)

## Tech Stack
- Terraform 1.10+
- GitHub Actions
- AWS (EC2, S3, IAM)
- S3 Native State Locking (use_lockfile)

## Key Features
- Remote State Management - S3 backend
- Native S3 Locking (use_lockfile=true) - No DynamoDB needed
- Secure AWS credentials via GitHub Secrets
- Auto deploy on push to main branch

## Project Structure
## How to Run Locally
```bash
# AWS credentials set करा
export AWS_ACCESS_KEY_ID="your-key"
export AWS_SECRET_ACCESS_KEY="your-secret"
export AWS_DEFAULT_REGION="ap-south-1"

# Initialize
terraform init

# Preview
terraform plan

# Deploy
terraform apply

# Destroy
terraform destroy
```

## CI/CD Pipeline Flow
1. Code push to main branch
2. GitHub Actions trigger
3. terraform init → plan → apply
4. Resources created on AWS
5. State saved to S3 bucket

## Interview Highlights
- S3 remote backend - team साठी shared state
- Native S3 locking - DynamoDB शिवाय concurrent apply protection
- GitHub Secrets - secure credential management
- Real errors debug केले - provider conflict, state mismatch, credential issues

## Author
Kishor Kalamkar
GitHub: github.com/kalamkarkishor1993
EOF




