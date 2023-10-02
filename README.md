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
<!-- BEGIN_TF_DOCS -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_google"></a> [google](#provider\_google) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [google_compute_router.router](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_router) | resource |
| [google_compute_router_nat.nats](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_router_nat) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_bgp"></a> [bgp](#input\_bgp) | BGP information specific to this router. | `any` | `null` | no |
| <a name="input_description"></a> [description](#input\_description) | An optional description of this resource | `string` | `null` | no |
| <a name="input_name"></a> [name](#input\_name) | Name of the router | `string` | n/a | yes |
| <a name="input_nats"></a> [nats](#input\_nats) | NATs to deploy on this router. | `any` | `[]` | no |
| <a name="input_network"></a> [network](#input\_network) | A reference to the network to which this router belongs | `string` | n/a | yes |
| <a name="input_project"></a> [project](#input\_project) | The project ID to deploy to | `string` | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | Region where the router resides | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_router"></a> [router](#output\_router) | The created router |
<!-- END_TF_DOCS -->