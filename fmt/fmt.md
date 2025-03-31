# Terraform Command: terraform fmt

## What is terraform fmt?
The terraform fmt command is used to format your Terraform configuration files (.tf and .tfvars) according to the canonical style conventions. It ensures your code is clean, consistent, and easier to read.

- It automatically fixes indentation, spacing, and alignment issues  
- It’s a great way to enforce best practices and maintain a consistent coding style across your team  

## Example Scenario
Imagine you are writing a Terraform configuration to create an Azure Resource Group and a Storage Account. However, the code is poorly formatted and inconsistent. Let’s see how _terraform fmt_ can help.

## Run terraform fmt
Open your terminal, navigate to the directory containing the main.tf file, and run:
```bash
terraform init
terraform fmt
```

## Expected Output
If the file was successfully formatted, you will see:
```bash
main.tf
```

This indicates that the main.tf file was updated to follow Terraform's formatting standards.

## Check the Updated File
Open the main.tf file again, and you’ll see that it has been reformatted to look like this:

## Formatted Terraform Configuration (main.tf)
