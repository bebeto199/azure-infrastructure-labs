# Lab 07 - Terraform Deployment

## Objective
Deploy Azure resources using Terraform.

## main.tf

```hcl
provider "azurerm" {
  features {}
}

resource "azurerm_resource_group" "rg" {
  name     = "lab-rg"
  location = "East US"
}
