# Terraform Command: terraform plan

## What is terraform plan?
The terraform plan command is used to create an execution plan. It shows you what Terraform will do when you run terraform apply. Specifically, it:

- Compares the current state of your infrastructure (from the state file) with your configuration files  
- Previews the changes Terraform will make to your infrastructure (e.g., resources to be created, updated, or destroyed)  
- Does not make any changes to your infrastructure—it's a dry run.  

This command is essential for reviewing changes before applying them to avoid unintended modifications.  

## Example Scenario
Imagine you are writing a Terraform configuration to create an Azure Resource Group and a Storage Account. Let’s see how terraform plan works in this context.


## Initialize the Project
Run terraform init to initialize the working directory and download the required provider plugins:
```bash
terraform init
```

Generate the execution plan by running:
```bash
terraform plan
```

## Expected Output
Terraform will analyze the configuration and show a detailed plan of the changes it will make. The output will look something like this:  

```yaml
Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  # azurerm_resource_group.example_rg will be created
  + resource "azurerm_resource_group" "example_rg" {
      + id       = (known after apply)
      + location = "East US"
      + name     = "example-resource-group"
    }

  # azurerm_storage_account.example_storage will be created
  + resource "azurerm_storage_account" "example_storage" {
      + id                     = (known after apply)
      + location               = "East US"
      + name                   = "examplestorageacct"
      + resource_group_name    = "example-resource-group"
      + account_tier           = "Standard"
      + account_replication_type = "LRS"
    }

Plan: 2 to add, 0 to change, 0 to destroy.

------------------------------------------------------------------------

Note: You didn't specify an "-out" parameter to save this plan, so Terraform can't guarantee that exactly these actions will be performed if "terraform apply" is subsequently run.
```

## Key points in the output:

### + create: Indicates resources that will be created.
### Plan: 2 to add, 0 to change, 0 to destroy: Summarizes the actions Terraform will take.
