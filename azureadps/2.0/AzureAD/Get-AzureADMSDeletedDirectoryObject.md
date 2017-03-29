---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version:
schema: 2.0.0
updated_at: 03/18/2017 00:03 AM
ms.date: 03/18/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Get-AzureADMSDeletedDirectoryObject.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Get-AzureADMSDeletedDirectoryObject.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/1263ae8ffe474c57d7a10e2353316c0deac8aa18
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: carolz
---

# Get-AzureADMSDeletedDirectoryObject

## SYNOPSIS
This cmdlet is used to retrieve a deleted directory object from the directory

## SYNTAX

```
Get-AzureADMSDeletedDirectoryObject -Id <String>
```

## DESCRIPTION
This cmdlet is used to retrieve a deleted directory object from the directory

## EXAMPLES

### Example 1
```
Get-AzureADMSDeletedDirectoryObject -Id 85b5ff1e-0402-400c-9e3c-0f9e965325d1
```

This example shows how to retrieve the deleted directory object with id = 85b5ff1e-0402-400c-9e3c-0f9e965325d1 from the directory

## PARAMETERS

### -Id
The Id of the directory object to retrieve

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

