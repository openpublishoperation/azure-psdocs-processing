---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version:
schema: 2.0.0
updated_at: 03/29/2017 02:03 AM
ms.date: 03/29/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure/v3.7.0/Get-AzureNetworkInterfaceConfig.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure/v3.7.0/Get-AzureNetworkInterfaceConfig.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/828e5b8648af6bdf3119ffe0cd409647f00de183
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureNetworkInterfaceConfig

## SYNOPSIS

## SYNTAX

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

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

### -Name
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

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

[Add-AzureNetworkInterfaceConfig](./Add-AzureNetworkInterfaceConfig.md)

[Remove-AzureNetworkInterfaceConfig](./Remove-AzureNetworkInterfaceConfig.md)

[Set-AzureNetworkInterfaceConfig](./Set-AzureNetworkInterfaceConfig.md)


