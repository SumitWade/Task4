### Project Title

# Terraform Docker Container Project

A simple Terraform project that provisions a local Docker container using the Docker provider. Ideal for learning Terraform basics and local container orchestration.

Repository: [`SumitWade/Task4`](https://github.com/SumitWade/Task4.git)

-----

### 🚀 Installation

#### 1. Clone the repository

```bash
git clone https://github.com/SumitWade/Task4.git
cd Task4
```

#### 2. Install prerequisites

- Docker Desktop (Windows 10/11)
  - Download: `https://www.docker.com/products/docker-desktop/`
- Terraform CLI (>= 1.3.0)
  - Download: `https://developer.hashicorp.com/terraform/downloads`

Ensure Docker Desktop is running and the Docker engine is started before proceeding.

-----

### ✅ Steps to Complete the Task

#### 1. Initialize Terraform

Initialize the project and download the Docker provider.

```bash
terraform init
```

#### 2. Plan the Deployment

See what Terraform will create.

```bash
terraform plan
```

#### 3. Apply the Configuration

Provision the Docker image and container.

```bash
terraform apply -auto-approve
```

#### 4. Verify the Resources

Confirm the container is running and accessible.

```bash
docker ps
curl http://localhost:8080/
```

#### 5. Clean Up

Destroy the resources to revert your environment.

```bash
terraform destroy -auto-approve
```

-----

### 📦 What this project creates

- `docker_image.nginx`: Pulls `nginx:latest` (kept locally)
- `docker_container.nginx`: Runs container `terraform-nginx` mapping `8080:80`

-----

### 🧾 Logs (optional)

Capture Terraform logs to files (Windows):

```bash
terraform init 1> terraform-init.log 2>&1
terraform apply -auto-approve 1> terraform-apply.log 2>&1
terraform destroy -auto-approve 1> terraform-destroy.log 2>&1
```

-----

### 📚 What We Learned

- How to structure a Terraform project for local Docker usage
- How to provision and manage a container via Terraform
- Key commands: `init`, `plan`, `apply`, and `destroy`
- Good practices for capturing logs and verifying outcomes locally

-----

### 🙌 Author

- Name: Sumit Wade
- Internship: DevOps Internship Task 4

