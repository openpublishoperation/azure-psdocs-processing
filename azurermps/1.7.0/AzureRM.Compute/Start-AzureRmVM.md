---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 0447A463-CF47-4EF7-8FB7-C0612499F3B0
updated_at: 11/01/2016 22:11 PM
ms.date: 11/01/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v1.3.4/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v1.3.4/Start-AzureRmVM.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/f59f3ef60bc592383812213e69fd77ba950759ed
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Start-AzureRmVM

## SYNOPSIS
Starts an Azure virtual machine.

## SYNTAX

### ResourceGroupNameParameterSetName (Default)
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### IdParameterSetName
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.

## EXAMPLES

### Example 1: Start a virtual machine
```
PS C:\>Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.

## PARAMETERS

### -Name
Specifies the name of the virtual machine to start.

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

### -ResourceGroupName
Specifies the name of the resource group of the virtual machine.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
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

### -Id
Specifies the Resource ID of the virtual machine.

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
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

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVM](./New-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Restart-AzureRmVM](./Restart-AzureRmVM.md)

[Stop-AzureRmVM](./Stop-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


