# My DevOps App

A full-stack DevOps project built from scratch — featuring a Node.js web app with a complete CI/CD pipeline, Docker containerisation, and AWS infrastructure managed with Terraform.

## Live App
http://51.21.245.145

## Tech Stack
- **App:** Node.js + Express
- **Containerisation:** Docker
- **CI/CD:** GitHub Actions
- **Infrastructure:** Terraform
- **Hosting:** AWS EC2

## How it works
1. Code is pushed to GitHub
2. GitHub Actions automatically triggers
3. Docker image is built and pushed to Docker Hub
4. App is automatically deployed to AWS EC2

## Project Structure
my-devops-app/
├── .github/workflows/   # CI/CD pipeline
├── public/              # Frontend
├── terraform/           # AWS infrastructure as code
├── app.js               # Node.js server
└── Dockerfile           # Container config
## Infrastructure
All AWS infrastructure is managed with Terraform:
- EC2 instance (t3.micro)
- Security group (ports 22 and 80)

To recreate the infrastructure:
```bash
cd terraform
terraform init
terraform apply
```

## Local Development
```bash
npm install
node app.js
# visit http://localhost:3000
```

## CI/CD Pipeline
Every push to main branch automatically:
- Builds a Docker image
- Pushes to Docker Hub
- Deploys to AWS EC2