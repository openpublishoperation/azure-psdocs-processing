---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 8E2FBF2A-2262-49B6-8C23-6CD22CA1E37D
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.RecoveryServices/v2.1.0/Get-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.RecoveryServices/v2.1.0/Get-AzureRmRecoveryServicesBackupProperties.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureRmRecoveryServicesBackupProperties

## SYNOPSIS
Gets Backup properties.

## SYNTAX

```
Get-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmRecoveryServicesBackupProperties** cmdlet gets backup properties for a Recovery Services vault.

## EXAMPLES


## PARAMETERS

### -Vault
Specifies the name of the vault.
The vault must be an **AzureRmRecoveryServicesVault** object.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-AzureRmRecoveryServicesBackupProperties](./Set-AzureRmRecoveryServicesBackupProperties.md)
