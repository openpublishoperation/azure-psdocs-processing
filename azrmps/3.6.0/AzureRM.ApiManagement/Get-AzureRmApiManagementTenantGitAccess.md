---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7E2D1A79-C6A6-4422-B190-6C01B6EAD2FC
online version:
schema: 2.0.0
updated_at: 03/14/2017 00:03 AM
ms.date: 03/14/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/marchrelease/azureps-cmdlets-docs/ResourceManager/AzureRM.ApiManagement/v3.4.0/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/marchrelease/azureps-cmdlets-docs/ResourceManager/AzureRM.ApiManagement/v3.4.0/Get-AzureRmApiManagementTenantGitAccess.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/e504ae03e3e2dd3ac42031d5ca637c489fa8b76b
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-AzureRmApiManagementTenantGitAccess

## SYNOPSIS
Gets the Git access configuration for a tenant.

## SYNTAX

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.

## EXAMPLES

### Example 1: Get tenant access configuration
```
PS C:\> Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

This command gets the Git access configuration for the specified context.

## PARAMETERS

### -Context
Specifies a **PsApiManagementContext** object.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation

## NOTES

## RELATED LINKS

[Get-AzureRmApiManagementTenantSyncState](./Get-AzureRmApiManagementTenantSyncState.md)
