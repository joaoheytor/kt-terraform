# What is terraform validate?

The terraform validate command checks the syntax and internal consistency of your Terraform configuration files. It ensures your *.tf* files are well-formed and adhere to Terraform's requirements, but it does not check external dependencies (_e.g., whether the Azure subscription is authenticated or the resource exists_).

## Run terraform validate
Open your terminal, navigate to the directory containing the *main.tf* file, and run:

```bash
terraform init
terraform validate
```

## Expected Output
If the configuration is valid, you will see:
```bash
Success! The configuration is valid.
```

## Introduce an Error
To demonstrate how terraform validate catches errors, modify the main.tf file and introduce a typo. For example, change *account_tier* to *tier* (which is not a valid argument for the azurerm_storage_account resource):
```yaml
resource "azurerm_storage_account" "example_storage" {
  name                     = "examplestorageacct"
  resource_group_name      = azurerm_resource_group.example_rg.name
  location                 = azurerm_resource_group.example_rg.location
  tier                     = "Standard"  # Invalid argument
  account_replication_type = "LRS"
}
```

## Run terraform validate Again
Run the command again:
```bash
terraform validate
```

## Expected Output
Terraform will detect the error and display a message like:
```bash
Error: Unsupported argument
An argument named "tier" is not expected here. Did you mean "account_tier"?
```
