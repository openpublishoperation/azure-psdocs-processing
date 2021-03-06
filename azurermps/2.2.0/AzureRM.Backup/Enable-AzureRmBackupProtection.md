---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: CE716B6E-0D99-40F0-ACD9-8B81C33BBE2F
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Backup/v2.1.0/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Backup/v2.1.0/Enable-AzureRmBackupProtection.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Enable-AzureRmBackupProtection

## SYNOPSIS
Associates an item with an Azure Backup protection policy.

## SYNTAX

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.
To enable a protection policy, you must first have an existing backup item and an existing policy.
Both must belong to the same Backup vault.
The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.

## EXAMPLES

### Example 1: Enable protection on an Azure virtual machine
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.
The command stores that object in the $Vault variable.

The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.
The command stores that object in the $Policy variable.

The final command uses the pipeline operator to pass values from one cmdlet to the next.
It gets a container, by using the Get-AzureRmBackupContainer cmdlet.
The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.
The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.

## PARAMETERS

### -Item
Specifies the Backup item for which this cmdlet enables protection.
To obtain an **AzureRmBackupItem**, use the Get-AzureRmBackupItem cmdlet.

```yaml
Type: AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Policy
Specifies protection policy that this cmdlet associates with an item.
To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### AzureRmBackupItem

## OUTPUTS

### AzureRmBackupJob

## NOTES

## RELATED LINKS

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


