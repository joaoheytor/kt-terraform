# **Terraform Exercise: Deploying Azure Resources**

## **Exercise Proposal**

### **Scenario**
Your company, **TechCorp**, is expanding its cloud infrastructure to support a new internal application. As part of this initiative, you need to deploy the following resources in Azure:

1. **Resource Group**: A logical container to group all related resources.
2. **Storage Account**: To store application logs and other data.
3. **Virtual Machine**: A Linux-based VM to host the application.

The infrastructure should be deployed in the **East US** region. The team has provided the following requirements:

### **Requirements**
1. **Resource Group**:
   - Name: `techcorp-<YOUR_NAME>-rg`
   - Location: `East US`

2. **Storage Account**:
   - Name: `techcorpstorageacct` (must be globally unique).
   - Account Tier: `Standard`
   - Replication Type: `LRS` (Locally Redundant Storage)

3. **Virtual Machine**:
   - Name: `techcorp-vm`
   - Size: `Standard_B1s`
   - OS: Ubuntu 20.04 LTS
   - Admin Username: `adminuser`
   - Admin Password: `P@ssw0rd1234!` (for simplicity in this exercise, but emphasize using secure methods like Key Vault in real scenarios).
   - Public IP: The VM should have a public IP for remote access.

4. **Network Resources** (for the VM):
   - Virtual Network: `techcorp-vnet` with a CIDR block of `10.0.0.0/16`.
   - Subnet: `techcorp-subnet` with a CIDR block of `10.0.1.0/24`.
   - Network Security Group (NSG): Allow SSH (port 22) traffic.

---

### **Tasks**
1. Write a Terraform configuration file (`main.tf`) to deploy the above resources.
2. Use variables for the following:
   - Resource Group name
   - Location
   - VM admin username
   - VM admin password
3. Initialize the Terraform project, validate the configuration, and apply it to deploy the resources.
4. Verify the resources in the Azure Portal.

---

### **Deliverables**
- A `main.tf` file with the Terraform configuration.
- A `variables.tf` file to define the variables.
- A `terraform.tfvars` file to provide values for the variables.
