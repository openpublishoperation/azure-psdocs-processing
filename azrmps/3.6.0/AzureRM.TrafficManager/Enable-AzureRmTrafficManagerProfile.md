---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version:
schema: 2.0.0
updated_at: 03/11/2017 23:03 PM
ms.date: 03/11/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.TrafficManager/v2.6.0/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.TrafficManager/v2.6.0/Enable-AzureRmTrafficManagerProfile.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/bc71000aa3c7f754b95442dcc415a7324626a15c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
---

# Enable-AzureRmTrafficManagerProfile

## SYNOPSIS
Enables a Traffic Manager profile.

## SYNTAX

### Fields
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### Object
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.
You can specify the profile object by using the pipeline or as a parameter value.
Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.

## EXAMPLES

### Example 1: Enable a profile specified by name
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

This command enables the profile named ContosoProfile in ResourceGroup11.

### Example 2: Enable a profile by using the pipeline
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

This command gets the profile named ContosoProfile in ResourceGroup11.
The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.
That cmdlet enables that profile.

## PARAMETERS

### -Name
Specifies the name of the Traffic Manager profile that this cmdlet enables.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of a resource group.
This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Specifies a **TrafficManagerProfile** object to enable.
To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Network.TrafficManagerProfile
This cmdlet accepts a **TrafficManagerProfile** object.

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-AzureRmTrafficManagerProfile](./Disable-AzureRmTrafficManagerProfile.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)

