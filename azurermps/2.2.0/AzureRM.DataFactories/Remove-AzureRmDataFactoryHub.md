---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: AD11DC70-2637-44F6-B502-9625BEF35C52
updated_at: 11/22/2016 20:11 PM
ms.date: 11/22/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.DataFactories/v2.1.0/Remove-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.DataFactories/v2.1.0/Remove-AzureRmDataFactoryHub.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/0cedc8f73bc96cf5ac4c69144e17b3de601fd3cc
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Remove-AzureRmDataFactoryHub

## SYNOPSIS
Removes a hub from Azure Data Factory.

## SYNTAX

### ByFactoryName (Default)
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Remove-AzureRmDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureRmDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.
If you remove a hub, all linked services and pipelines in the hub are also removed.

## EXAMPLES

### Example 1: Remove a hub
```
PS C:\>Remove-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.

## PARAMETERS

### -DataFactory
Specifies a **PSDataFactory** object.
This cmdlet removes a hub from the data factory that this parameter specifies.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Specifies the name of a data factory.
This cmdlet removes a hub from the data factory that this parameter specifies.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Indicates that this cmdlet removes a hub without prompting you for confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the hub to remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of an Azure resource group.
This cmdlet removes a hub from the group that this parameter specifies.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
* Keywords: azure, azurerm, arm, resource, management, manager, data, factories

## RELATED LINKS

[Get-AzureRmDataFactoryHub](./Get-AzureRmDataFactoryHub.md)

[New-AzureRmDataFactoryHub](./New-AzureRmDataFactoryHub.md)


