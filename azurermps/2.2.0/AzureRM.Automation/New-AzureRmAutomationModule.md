---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: C20D4D62-E8B6-4517-B9CD-82D24F0B9E21
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Automation/v2.1.0/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Automation/v2.1.0/New-AzureRmAutomationModule.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# New-AzureRmAutomationModule

## SYNOPSIS
Imports a module into Automation.

## SYNTAX

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLink] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.
This command accepts a compressed file that has a .zip file name extension.
The file contains a folder that includes a file that is one of the following types: 

- Windows PowerShell module, which has a .psm1 or .dll file name extension 
- Windows PowerShell module manifest, which has a .psd1 file name extension

The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.

Specify the .zip file as a URL that the Automation service can access.

If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.
The command finishes whether the import succeeds or fails.
To check whether it succeeded, run the following command:

`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName

Check the **ProvisioningState** property for a value of Succeeded.

## EXAMPLES

### Example 1: Import a module
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

This command imports a module named ContosoModule into the Automation account named Contoso17.
The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.

## PARAMETERS

### -AutomationAccountName
Specifies the name of the Automation account for which this cmdlet imports a module.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLink
Specifies the URL of the .zip file that contains a module that this cmdlet imports.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of the module that this cmdlet imports.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of a resource group for which this cmdlet imports a module.

```yaml
Type: String
Parameter Sets: (All)
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

## NOTES

## RELATED LINKS

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[Remove-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)

[Set-AzureRmAutomationModule](./Set-AzureRmAutomationModule.md)


