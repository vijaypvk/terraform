This Terraform configuration creates a Docker container running Nginx and exposes it on port 8080.

## **Prerequisites**

- Terraform installed on your system
- Docker installed and running on your system

## **Usage**

1. Initialize the Terraform working directory by running `terraform init`
2. Apply the Terraform configuration by running `terraform apply`
3. Verify that the Docker container is running by running `docker ps`

## **Configuration**

The Terraform configuration uses the following providers and resources:

- **Provider:** `docker` from `kreuzwerker/docker` (version `3.0.2`)
- **Resource:** `docker_image` named `nginx` with the following properties:
    - `name`: `nginx`
    - `keep_locally`: `false`
- **Resource:** `docker_container` named `nginx` with the following properties:
    - `image`: The image ID of the `nginx` Docker image
    - `name`: `test`
    - `ports`: Exposes port 80 internally and maps it to port 8080 externally

## **Note**

This configuration assumes that you have Docker installed and running on your system. You may need to modify the configuration to fit your specific use case.
