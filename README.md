# Terraform Bastion Host and Bastion Service

This creates a Bastion Host and a Bastion Service on Azure along with a VM within a private subnet that you would use a bastion to connect to. 
The Bastion host is its own vm with a public ip that can connect to the private subnets.
The Azure Basiton Service is a service managed by azure that can connect to the private subnets through the azure portal.

## Pre-requisites:
  Azure account - the free trial works with this at the time of creation <br/>
  Azure CLI tool <br/>
  Terraform
  
## Setup Account Permissions: 
  To authenticate terrafrom to azure [follow the guide provided by microsoft](https://docs.microsoft.com/en-us/azure/developer/terraform/authenticate-to-azure?tabs=bash)

## Terraform does it thing: <br/>
  initialize terraform provider versions <br/>
   `terraform init` <br/>
  validates if the terraform files are valid <br/>
   `terraform validate` <br/>
  
  ### Option 1 - Apply Terraform
  creates a plan to be executed<br/>
  `terraform plan`<br/>
  applioes terraform files to azure <br/>
  `terraform apply`
  
  ### Option 2 - Save a Plan to Execute
  creates and saves a plan to execute<br/>
  `terraform plan -out tfplan.out`<br/>
  applies the saved plan<br/>
  `terraform apply tfplan.out`
