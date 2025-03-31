# Terraform Command: terraform init

## What is terraform init?
The terraform init command is the first command you run when starting a new Terraform project. It initializes the working directory by:  

- Downloading the required provider plugins (e.g., azurerm for Azure)  
- Setting up the backend configuration (if specified) for storing the Terraform state  
- Preparing the directory for other Terraform commands like plan and apply  

Without running terraform init, you won’t be able to use other Terraform commands.  

# Example Scenario
Imagine you are starting a new Terraform project to create an Azure Resource Group and a Storage Account. Let’s see how terraform init works in this context.  

## Run terraform init
Open your terminal, navigate to the directory containing the main.tf file, and run:

```bash
terraform init
```

## Expected Output
Terraform will perform the following actions:  
- Download the azurerm provider plugin  
- Set up the working directory for Terraform commands  

The output will look something like this:  

```bash
Initializing the backend...

Initializing provider plugins...
- Finding hashicorp/azurerm versions matching ">= 3.0.0"...
- Installing hashicorp/azurerm v3.74.0...
- Installed hashicorp/azurerm v3.74.0 (signed by HashiCorp)

Terraform has been successfully initialized!
```

## Verify Initialization
After running terraform init, you’ll notice that Terraform has created a *.terraform* directory in your project folder. This directory contains the downloaded provider plugins and other initialization files.

