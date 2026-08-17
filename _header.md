![Coalfire](coalfire_logo.png)

# Google Cloud Router Terraform Module

This module handles opinionated Google Cloud Platform routing. Coalfire has tested this module with Terraform version 1.5.0 and the Hashicorp Google provider versions 4.70 - 5.0.

FedRAMP Compliance: Moderate

### Usage

```
module "cloud_router" {
    source = "github.com/Coalfire-CF/terraform-gcp-cloud-router"

    name = "router-name"
    project = "your-project"
    region = "us-central1"
    network = "your-network-id"
}
```
