---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: CA90AFD7-6DE6-497A-8EA2-DDC6B2F8FA1D
updated_at: 11/01/2016 22:11 PM
ms.date: 11/01/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v1.3.4/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v1.3.4/New-AzureRmVmssIpConfig.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/f59f3ef60bc592383812213e69fd77ba950759ed
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# New-AzureRmVmssIpConfig

## SYNOPSIS
Creates an IP configuration for a network interface of a VMSS.

## SYNTAX

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).
Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.

## EXAMPLES

### Example 1: Create an IP configuration object for a VMSS interface
```
PS C:\>$IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

This command creates an IP configuration object named ContosoVmssInterface02.
The command uses a previously defined subnet ID stored in $SubnetId.
The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.

### Example 2: Create an IP configuration object that includes NAT pool settings
```
PS C:\>$IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.
The command uses a previously defined subnet ID stored in $SubnetId.
The command stores the configuration settings in the $IPConfiguration variable for later use.
The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.

## PARAMETERS

### -Name
Specifies the name of the IP configuration.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Specifies an ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Specifies the subnet ID in which the configuration creates  the VMSS network interface.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolsId
Specifies an array of references to backend address pools of load balancers.
A scale set can reference backend address pools of one public and one internal load balancer.
Multiple scale sets cannot use the same load balancer.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.
A scale set can reference incoming NAT pools of one public and one internal load balancer.
Multiple scale sets cannot use the same load balancer.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Specifies an array of references to incoming NAT pools of the load balancers.
A scale set can reference incoming NAT pools of one public and one internal load balancer.
Multiple scale sets cannot use the same load balancer.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


