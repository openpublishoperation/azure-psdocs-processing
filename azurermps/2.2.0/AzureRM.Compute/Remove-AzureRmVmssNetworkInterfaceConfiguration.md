---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 0CF8A423-C7B7-4BFF-9352-3E20718DC3C5
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.1.0/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.1.0/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Remove-AzureRmVmssNetworkInterfaceConfiguration

## SYNOPSIS
Removes a network interface configuration from a VMSS.

## SYNTAX

```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).

## EXAMPLES

### Example 1: Remove an interface configuration
```
PS C:\>$VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.

The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.

## PARAMETERS

### -Name
Specifies the name of the network interface configuration that this cmdlet removes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifies the VMSS object.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


