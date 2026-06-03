# Task 0: codebase

All code is stored on Harness Code Repository.

![codebase](images/codebase.png)


The hello-world project consists of two applications:

The frontend app is a React SPA where you can list, add and delete todos.

The backend app is a Spring Boot application which provides the corresponding APIs and saves the todos into PostgreSQL, namely AWS RDS.

![aws](images/aws.svg)

# Task 1: Infrastructure as Code

Terraform code for creating AWS EKS and RDS can be found on Harness Code Repository.

# Task 2: Kubernetes

# Task 3: Pipeline as Code

## Task 3.1: Infra Pipeline

This hasn't been implemented yet.

To create EKS and RDS, clone the Terraform code from Harness Code Repoistory and run terraform.

For example, to set up EKS for dev environment:

```bash
cd clusters/dev/eks
terraform plan
terraform apply
```


## Task 3.1: Service Pipeline

These two CI pipelines are for building the apps and Docker images.

![ci](images/ci.png)

When new git commit or branch is pushed to code repository, the CI will be trigger automatically.

The app will be built using NPM or Gradle, and the Docker image will be published to Docker registry.

https://hub.docker.com/repository/docker/joekyo/todo-frontend-app/tags
https://hub.docker.com/repository/docker/joekyo/todo-backend-app/tags
