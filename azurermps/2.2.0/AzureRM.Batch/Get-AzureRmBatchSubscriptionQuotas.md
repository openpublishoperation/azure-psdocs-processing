---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: FCD7FE25-674A-4FF1-9691-A111D1964463
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Batch/v2.1.0/Get-AzureRmBatchSubscriptionQuotas.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Batch/v2.1.0/Get-AzureRmBatchSubscriptionQuotas.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureRmBatchSubscriptionQuotas

## SYNOPSIS
Gets the quota for your subscription in the Batch service for a region.

## SYNTAX

```
Get-AzureRmBatchSubscriptionQuotas [-Location] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmBatchSubscriptionQuotas** cmdlet gets the quota of accounts for your subscription in the Azure Batch service for the specified region.

## EXAMPLES

### Example 1: Get the quota for the subscription in the West US region
```
PS C:\>Get-AzureRmBatchSubscriptionQuotas -Location "westus"
AccountQuota Location
------------ --------
1            westus
```

This command gets the quota for the current subscription in the West US region.
The return value indicates that this subscription can create only one account in that region.

## PARAMETERS

### -Location
Specifies the region for which this cmdlet checks the quota.
For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions (https://azure.microsoft.com/en-us/regions).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### PSBatchSubscriptionQuotas

## NOTES

## RELATED LINKS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Azure Batch Cmdlets](./AzureRM.Batch.md)


