# **Steps to Deploy**
1. **Initialize the Project**:
   ```bash
   terraform init
   ```

2. **Validate the Configuration**:
   ```bash
   terraform validate
   ```

3. **Generate a Plan**:
   ```bash
   terraform plan
   ```

4. **Apply the Configuration**:
   ```bash
   terraform apply
   ```

5. **Verify the Resources**:
   - Check the Azure Portal to confirm the Resource Group, Storage Account, and Virtual Machine are created.

---

### **Bonus Challenge**
- Add a **Tag** to all resources (e.g., `Environment = "Development"`).
- Use a **remote backend** (e.g., Azure Blob Storage) to store the Terraform state file.
