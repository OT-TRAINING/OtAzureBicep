### Azure CLI Commands:

1. **Delete NSG (Network Security Group)**:
   
   ```bash
   az network nsg delete --name <nsg_name> --resource-group <resource_group_name>
   ```

2. **Delete NIC (Network Interface Card)**:

   ```bash
   az network nic delete --name <nic_name> --resource-group <resource_group_name>
   ```

3. **Delete Storage Account**:

   ```bash
   az storage account delete --name <storage_account_name> --resource-group <resource_group_name>
   ```

4. **Delete VNet (Virtual Network)**:

   ```bash
   az network vnet delete --name <vnet_name> --resource-group <resource_group_name>
   ```

### Azure PowerShell Commands:

1. **Delete NSG (Network Security Group)**:
   
   ```powershell
   Remove-AzNetworkSecurityGroup -Name <nsg_name> -ResourceGroupName <resource_group_name>
   ```

2. **Delete NIC (Network Interface Card)**:

   ```powershell
   Remove-AzNetworkInterface -Name <nic_name> -ResourceGroupName <resource_group_name>
   ```

3. **Delete Storage Account**:

   ```powershell
   Remove-AzStorageAccount -Name <storage_account_name> -ResourceGroupName <resource_group_name>
   ```

4. **Delete VNet (Virtual Network)**:

   ```powershell
   Remove-AzVirtualNetwork -Name <vnet_name> -ResourceGroupName <resource_group_name>
   ```

Replace `<nsg_name>`, `<nic_name>`, `<storage_account_name>`, `<vnet_name>`, and `<resource_group_name>` with the appropriate names and resource group where your resources are located.
8:06
To create a deployment using the `az deployment create` command with a specific deployment mode, you need to provide the necessary parameters such as the resource group, template file, parameters file (if any), and the deployment mode. Below are the commands for different deployment modes:

### Create Deployment with Incremental Mode:

In incremental mode, resources are added or updated in the resource group without deleting existing resources that are not included in the template.

```bash
az deployment create \
    --name <deployment_name> \
    --resource-group <resource_group_name> \
    --template-file <path_to_template_file> \
    --parameters @<path_to_parameters_file> \
    --mode Incremental
```

### Create Deployment with Complete Mode:

In complete mode, the resources in the resource group are replaced with the resources defined in the template. Existing resources not defined in the template are deleted.

```bash
az deployment create \
    --name <deployment_name> \
    --resource-group <resource_group_name> \
    --template-file <path_to_template_file> \
    --parameters @<path_to_parameters_file> \
    --mode Complete
```

### Create Deployment with Validation Mode:

In validation mode, the template is validated without creating any resources. This mode is useful for checking the syntax and structure of the template.

```bash
az deployment validate \
    --name <deployment_name> \
    --resource-group <resource_group_name> \
    --template-file <path_to_template_file> \
    --parameters @<path_to_parameters_file>
```

Replace `<deployment_name>`, `<resource_group_name>`, `<path_to_template_file>`, and `<path_to_parameters_file>` with your specific values.
