---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version:
schema: 2.0.0
updated_at: 03/29/2017 18:03 PM
ms.date: 03/29/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v3.7.0/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v3.7.0/Get-AzureRmLocation.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/347711259e2d6b4ccc2563e0a8c9e46b2fe2b824
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureRmLocation

## SYNOPSIS
Gets all locations and the supported resource providers for each location.

## SYNTAX

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.

## EXAMPLES

### Example 1: Get all locations and the supported resource providers
```
PS C:\> Get-AzureRmLocation
```

This command gets all locations and the supported resource providers for each location.

## PARAMETERS

### -ApiVersion
Specifies the API version that is supported by the resource Provider.
You can specify a different version than the default version.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
