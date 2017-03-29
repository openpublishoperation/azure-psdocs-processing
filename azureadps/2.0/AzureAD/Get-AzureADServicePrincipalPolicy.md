---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
ms.assetid: D4C305FF-6005-4296-8B26-CFFCACFF9D2C
online version:
schema: 2.0.0
updated_at: 03/28/2017 00:03 AM
ms.date: 03/28/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Get-AzureADServicePrincipalPolicy.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Get-AzureADServicePrincipalPolicy.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/9cd8b80caaebed24cf5986c4cc47381bc2c8e3b7
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: carolz
---

# Get-AzureADServicePrincipalPolicy

## SYNOPSIS

## SYNTAX

```
Get-AzureADServicePrincipalPolicy -Id <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADServicePrincipalPolicy** cmdlet gets the policy of a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a policy
```
PS C:\>Get-AzureADServicePrincipalPolicy -ObjectId "<object id of service principal>"
```

This command get the policy for the specified service principal.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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

### -Id
The ID of the Service Principal for which you want to retrieve the policy

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureADServicePrincipalPolicy](./Add-AzureADServicePrincipalPolicy.md)

[Remove-AzureADServicePrincipalPolicy](./Remove-AzureADServicePrincipalPolicy.md)

