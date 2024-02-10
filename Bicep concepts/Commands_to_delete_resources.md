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
