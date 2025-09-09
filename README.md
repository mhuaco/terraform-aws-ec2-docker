# terraform-aws-ec2-bootstrap

Bootstrap an AWS EC2 instance with Terraform, Docker, and MongoDB shell.

This repository provides a Terraform configuration to provision an Amazon Linux 2 EC2 instance in your default VPC. It automatically sets up:

- Security group with HTTP, SSH, and common dev ports
- Docker and Docker Compose
- MongoDB shell (`mongosh`) for connecting to MongoDB databases

Ideal for developers or DevOps engineers who want a preconfigured EC2 environment for testing and development.
