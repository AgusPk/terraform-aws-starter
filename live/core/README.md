# Core Infrastructure

This is where we keep our infrastructure as code for our cloud infrastructure.

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html)

## Initialize

```sh
terraform init
```

## 🚀 Deploy

> NOTE: In this example, we are using the `staging` environment and the `us-west-2` region.
> You can change these values to match your environment and region.

```sh
terraform plan -var-file ./configs/staging.us-west-2.tfvars -out ./staging.tfplan
terraform apply ./staging.tfplan
```

## 💣 Destroy

> NOTE: In this example, we are using the `staging` environment and the `us-west-2` region.
> You can change these values to match your environment and region.

```sh
terraform destroy -var-file ./configs/staging.us-west-2.tfvars
```
