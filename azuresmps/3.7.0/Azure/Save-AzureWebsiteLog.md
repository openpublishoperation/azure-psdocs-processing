---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version:
schema: 2.0.0
updated_at: 03/29/2017 02:03 AM
ms.date: 03/29/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure/v3.7.0/Save-AzureWebsiteLog.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure/v3.7.0/Save-AzureWebsiteLog.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/828e5b8648af6bdf3119ffe0cd409647f00de183
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Save-AzureWebsiteLog

## SYNOPSIS
Downloads and saves the logs for a specified website.

## SYNTAX

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.
To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.

The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.

## EXAMPLES

### Example 1: Download and save logs for a website
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.

## PARAMETERS

### -Name
Specifies the name of the website.

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

### -Output
Specifies the path to store the downloaded file.

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

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Specifies the slot name.

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

[Restore-AzureWebsiteDeployment](./Restore-AzureWebsiteDeployment.md)


