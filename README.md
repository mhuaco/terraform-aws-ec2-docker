## Quick Start: Preconfigured EC2 for Tyk

This Terraform project provisions an **AWS EC2 instance already set up for Tyk**, including Docker, Docker Compose, and required ports.

### Features
- Docker and Docker Compose installed
- Ports open:
  - **3000** → Tyk Dashboard
  - **8080** → Tyk Gateway
  - **22** → SSH
  - **80** → HTTP
- Preconfigured security group

### Setup Steps
1. Change the EC2 **tag name** in **`main.tf`** to differentiate this environment from others.  
   The tag is located here:
   ```hcl
   tags = { 
     Name = "mhuaco-instance"
   }
2. Create your own **AWS key pair**.
3. Update the Terraform variable in **`variables.tf`** to point to your key:

```hcl
variable "aws_key_pair" {
  default = "/path/to/your-key.pem"
  type    = string
}

Replace /path/to/your-key.pem with the location where you saved your key.
