---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version:
schema: 2.0.0
updated_at: 03/18/2017 00:03 AM
ms.date: 03/18/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Restore-AzureADMSDeletedDirectoryObject.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Restore-AzureADMSDeletedDirectoryObject.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/1263ae8ffe474c57d7a10e2353316c0deac8aa18
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
---

# Restore-AzureADMSDeletedDirectoryObject

## SYNOPSIS
This cmdlet is used to restore a previously deleted object.

## SYNTAX

```
Restore-AzureADMSDeletedDirectoryObject -Id <String>
```

## DESCRIPTION
This cmdlet is used to restore a previously deleted object. Currently, only restoring Group and Application objects is supported. 
When a group or an application is deleted it is initially soft deleted and can be recovered during the first 30 days after deletion. After 30 days the deleted object is permanently deleted and can no longer be recovered. 

## EXAMPLES

### Example 1
```
Restore-AzureADMSDeletedDirectoryObject -Id aa644285-eb75-4389-885e-7233f096984c
```

This example shows how to restore a deleted object with Id aa644285-eb75-4389-885e-7233f096984c 

## PARAMETERS

### -Id
The Id of the directory object to restore

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

