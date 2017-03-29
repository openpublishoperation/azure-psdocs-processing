---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 8CCEA18B-C9DC-4CC0-979B-66C776A06BC1
updated_at: 11/01/2016 22:11 PM
ms.date: 11/01/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Insights/v1.0.12/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Insights/v1.0.12/New-AzureRmAlertRuleEmail.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/f59f3ef60bc592383812213e69fd77ba950759ed
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# New-AzureRmAlertRuleEmail

## SYNOPSIS
Creates an email action for an alert rule.

## SYNTAX

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.

## EXAMPLES

### Example 1: Create an alert rule email action for service owners
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

This command creates an alert rule email action to send for its service owners when an alert rule is fired.

### Example 2: Create an alert rule email action for non-service owners
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

This command creates an alert rule email action for the specified email addresses, but not for the service owners.

### Example 3: Create an alert rule email action for service owners and non-service owners
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

This command creates an alert rule email action for the specified address and for its service owners.

## PARAMETERS

### -CustomEmails
Specifies a list of comma-separated e-mail addresses.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SendToServiceOwners
Indicates that this operation sends an e-mail to the service owners when the rule fires.

```yaml
Type: SwitchParameter
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

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[New-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


