---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version:
schema: 2.0.0
updated_at: 03/11/2017 02:03 AM
ms.date: 03/11/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v3.6.0/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v3.6.0/Move-AzureRmExpressRouteCircuit.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/04f63f6e685743ace2c57eb157574e34e8610b1c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Move-AzureRmExpressRouteCircuit

## SYNOPSIS

Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.

## SYNTAX

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic
deployment model to the Resource Manager deployment model. After the move, the ExpressRoute circuit
behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager
deployment model. Circuit links, virtual networks, and VPN gateways are not moved through this
operation. Those resources need to be reconfigured after the move.

## EXAMPLES

### Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model

```powershell
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## PARAMETERS

### -Name

The name of the ExpressRoute circuit to be moved.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName

The name of the resource group that will contain the ExpressRoute circuit being moved.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location

The name of the Azure location where the ExpressRoute circuit resides.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceKey

The Service Key used by the ExpressRoute circuit in the classic deployment model.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag

A hashtable of resource tags to be assigned to the circuit.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force

Forces the command to run without asking for user confirmation.

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

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose,
-WarningAction, and -WarningVariable. For more information, see about_CommonParameters
(http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[New-AzureRmExpressRouteCircuit](./New-AzureRmExpressRouteCircuit.md)

[Remove-AzureRmExpressRouteCircuit](./Remove-AzureRmExpressRouteCircuit.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
