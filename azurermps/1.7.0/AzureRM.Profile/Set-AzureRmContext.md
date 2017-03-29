---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 79BF6173-959C-45AC-B006-07D0D389C321
updated_at: 11/01/2016 22:11 PM
ms.date: 11/01/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Profile/v1.0.12/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Profile/v1.0.12/Set-AzureRmContext.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/f59f3ef60bc592383812213e69fd77ba950759ed
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Set-AzureRmContext

## SYNOPSIS
Sets the tenant, subscription, and environment for cmdlets to use in the current session.

## SYNTAX

### SubscriptionName (Default)
```
Set-AzureRmContext [-SubscriptionName <String>] [-WhatIf] [-Confirm] [-TenantId <String>] [<CommonParameters>]
```

### Context
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SubscriptionId
```
Set-AzureRmContext [-WhatIf] [-Confirm] [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureRmContext** cmdlet sets authentication information for cmdlets that you run in the current session.
The context includes tenant, subscription, and environment information.

## EXAMPLES

### Example1: Set the subscription context
```
PS C:\>Set-AzureRmContext -SubscriptionId 'xxxx-xxxx-xxxx-xxxx'
Account: PFuller@contoso.com

Environment: AzureCloud

Subscription: xxxx-xxxx-xxxx-xxxx

Tenant: yyyy-yyyy-yyyy-yyyy
```

This command sets the context to use the specified subscription.
This example uses placeholder values for the subscription ID and tenant ID.

## PARAMETERS

### -SubscriptionId
Specifies the subscription ID for the context that this cmdlet sets for the current session.

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the ID of the tenant for the context that this cmdlet sets for the current session.

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
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

### -Context
Specifies context for the current session as a **PSAzureContext** object.
To obtain context information, use the Get-AzureRmContext cmdlet.

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SubscriptionName
Specifies the subscription name for the context that this cmdlet sets for the current session.

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## RELATED LINKS

[Get-AzureRmContext](./Get-AzureRmContext.md)


