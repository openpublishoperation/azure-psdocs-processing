---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version:
schema: 2.0.0
updated_at: 03/29/2017 18:03 PM
ms.date: 03/29/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v3.7.0/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v3.7.0/Get-AzureRmProviderOperation.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/1b0e8fcdd474515f4a6eeac956865e25badf43bd
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureRmProviderOperation

## SYNOPSIS
Gets the operations for an Azure resource provider that are securable using Azure RBAC.

## SYNTAX

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
```

## DESCRIPTION
The **Get-AzureRmProviderOperation** gets the operations exposed by Azure resource providers.
Operations can be composed to create custom roles in Azure RBAC.
The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display.

Use **Get-AzureRmProviderOperation** * to get all operations for all Azure resource providers.

Use **Get-AzureRmProviderOperation** Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.

## EXAMPLES

### Example 1: Get all actions for all providers 


```
PS C:\> Get-AzureRmProviderOperation *
```

### --------------------------  Get actions for a particular resource provider  --------------------------


```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### --------------------------  Get all actions that can be performed on virtual machines  --------------------------


```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## PARAMETERS

### -OperationSearchString
The operation search string (with possible wildcard (*) characters)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES
Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## RELATED LINKS
