---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version:
schema: 2.0.0
updated_at: 03/18/2017 00:03 AM
ms.date: 03/18/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Remove-AzureADMSDeletedDirectoryObject.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Remove-AzureADMSDeletedDirectoryObject.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/1263ae8ffe474c57d7a10e2353316c0deac8aa18
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
---

# Remove-AzureADMSDeletedDirectoryObject

## SYNOPSIS
This cmdlet is used to permanently delete a previously deleted directory object

## SYNTAX

```
Remove-AzureADMSDeletedDirectoryObject -Id <String>
```

## DESCRIPTION
This cmdlet is used to permanently delete a previously deleted directory object. When a directory object is permanently deleted it can no longer be restored.

## EXAMPLES

### Example 1
```
Remove-AzureADMSDeletedDirectoryObject -Id aa644285-eb75-4389-885e-7233f096984c
```

This example shows how to permanently delete a previously deleted directory object with Id = aa644285-eb75-4389-885e-7233f096984c

## PARAMETERS

### -Id
The Id of the directory object that is permanently deleted

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

### System.String


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

