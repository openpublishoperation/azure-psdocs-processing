---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: D95D10F9-C7D0-4EC9-B0DA-CDD1BE66BBA3
updated_at: 11/11/2016 23:11 PM
ms.date: 11/11/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Automation/v2.1.0/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Automation/v2.1.0/Set-AzureRMAutomationCredential.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/79eeb985ea480979357fb4695832a0c3d29a48bf
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Set-AzureRmAutomationCredential

## SYNOPSIS
Modifies an Automation credential.

## SYNTAX

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.

## EXAMPLES

### Example 1: Update a credential
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

The first command assigns a user name to the $User variable.

The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.
The command stores that object in the $Password variable.

The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.

The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.

## PARAMETERS

### -AutomationAccountName
Specifies the name of the Automation account for which this cmdlet modifies a credential.

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

### -Description
Specifies a description for the credential that this cmdlet modifies.

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

### -Name
Specifies the name of the credential that this cmdlet modifies.

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
Specifies the name of the resource group for which this cmdlet modifies a credential.

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

### -Value
Specifies the credentials as a **PSCredential** object.

```yaml
Type: PSCredential
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

### Microsoft.Azure.Commands.Automation.Model.CredentialInfo

## NOTES

## RELATED LINKS

[Get-AzureRmAutomationCredential](./Get-AzureRMAutomationCredential.md)

[New-AzureRmAutomationCredential](./New-AzureRMAutomationCredential.md)

[Remove-AzureRmAutomationCredential](./Remove-AzureRMAutomationCredential.md)


