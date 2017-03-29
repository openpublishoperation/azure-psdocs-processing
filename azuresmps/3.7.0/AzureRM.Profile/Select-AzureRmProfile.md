---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version:
schema: 2.0.0
updated_at: 03/27/2017 18:03 PM
ms.date: 03/27/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/AzureRM.Profile/v2.7.0/Select-AzureRmProfile.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/AzureRM.Profile/v2.7.0/Select-AzureRmProfile.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4481ba5d382a258a76528a60b3c1580b75fdff10
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Select-AzureRmProfile

## SYNOPSIS
Loads Azure authentication information from a file.

## SYNTAX

### InMemoryProfile
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### ProfileFromDisk
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## DESCRIPTION
The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.
Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.

## EXAMPLES

### Example 1: Selecting a profile from a PSAzureProfile
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.

### Example 2: Selecting a profile from a JSON file
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

This example selects a profile from a JSON file that is passed through to the cmdlet. This JSON file can be created from Save-AzureRmProfile.

## PARAMETERS

### -Path
Specifies the path to profile information saved by using Save-AzureRMProfile.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### PSAzureProfile

## NOTES

## RELATED LINKS

[Get-AzureRMContext]()

