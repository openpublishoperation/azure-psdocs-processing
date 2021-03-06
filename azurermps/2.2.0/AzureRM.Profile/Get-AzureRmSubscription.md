---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: D6327A7C-C24A-42D1-B4D6-B026D23C89E3
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Profile/v2.1.0/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Profile/v2.1.0/Get-AzureRmSubscription.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureRmSubscription

## SYNOPSIS
Gets subscriptions that the current account can access.

## SYNTAX

### ListByIdInTenant (Default)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### ListByNameInTenant
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmSubscription** cmdlet gets the subscription ID, subscription name, and home tenant for Azure subscriptions that the current account can access.

## EXAMPLES

### Example 1: Get all subscriptions for a specific tenant
```
PS C:\>Get-AzureRmSubscription -TenantId 'xxxx-xxxx-xxxx-xxxx'
SubscriptionId: yyyy-yyyy-yyyy-yyyy
TenantId: xxxx-xxxx-xxxx-xxxx
Subscription Name: Contoso Subscription 1


SubscriptionId: yyyy-yyyy-yyyy-yyyy
TenantId: xxxx-xxxx-xxxx-xxxxSubscription Name: Contoso Subscription 2
```

This cmdlet displays the subscriptions in the given tenant that are authorized for the current account.
These examples use placeholder values for the tenant ID and the subscription ID.

### Example 2: Get all subscriptions in the current tenant
```
PS C:\>Get-AzureRmSubscription
SubscriptionId: yyyy-yyyy-yyyy-yyyy
TenantId: xxxx-xxxx-xxxx-xxxx
Subscription Name: Contoso Subscription 1


SubscriptionId: yyyy-yyyy-yyyy-yyyy
TenantId: xxxx-xxxx-xxxx-xxxx
Subscription Name: Contoso Subscription 2
```

This command gets all subscriptions in the current tenant that are authorized for the current user.

### Example 3: Change the current context to use a specific subscription
```
PS C:\>Get-AzureRmSubscription -SubscriptionId 'xxxx-xxxx-xxxx-xxxx' -TenantId 'yyyy-yyyy-yyyy-yyyy' | Set-AzureRmContext
SubscriptionId: xxxx-xxxx-xxxx-xxxx
TenantId: yyyy-yyyy-yyyy-yyyy
Subscription Name: Contoso Subscription 1
```

This command gets the specified subscription, and then passes it to the Set-AzureRmContext cmdlet by using the pipeline operator.
That cmdlet sets the current context to use that subscription.
By default, all subsequent cmdlets in this session use the specified subscription.

## PARAMETERS

### -SubscriptionId
Specifies the ID of the subscription to get.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Specifies the name of the subscription to get.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the ID of the tenant that contains subscriptions to get.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-AzureRmContext](./Set-AzureRmContext.md)


