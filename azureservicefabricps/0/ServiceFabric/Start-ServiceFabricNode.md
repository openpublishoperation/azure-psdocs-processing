---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 368529F1-EA7E-407B-93A7-352ED6D2048C
online version:
schema: 2.0.0
updated_at: 03/13/2017 21:03 PM
ms.date: 03/13/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricNode.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/16a82fb62f024a7a246aebb83519e457a923b5e1
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Start-ServiceFabricNode

## SYNOPSIS
**OBSOLETE**. Please use the [Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md) cmdlet instead.

## SYNTAX

```
Start-ServiceFabricNode [-NodeName] <String> [[-NodeInstanceId] <BigInteger>] [[-IpAddressOrFQDN] <String>]
 [[-ClusterConnectionPort] <Int32>] [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
**OBSOLETE**. The **Start-ServiceFabricNode** cmdlet starts a node in a Service Fabric cluster.

## PARAMETERS

### -ClusterConnectionPort
Specifies the cluster connection port for the node to start.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CommandCompletionMode
Specifies whether the action waits for the restart to complete.

```yaml
Type: CompletionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpAddressOrFQDN
Specifies the IP address or fully qualified domain name (FQDN) for the node to start.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeInstanceId
Specifies a node instance ID.

```yaml
Type: BigInteger
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
Specifies the name of a Service Fabric node to start.

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

### -TimeoutSec
Specifies the time-out period, in seconds, for the operation.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
Specifies the name of a Service Fabric node.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Testability.StartNodeResult** object that represents the operation result.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Disable-ServiceFabricNode](./Disable-ServiceFabricNode.md)

[Enable-ServiceFabricNode](./Enable-ServiceFabricNode.md)

[Get-ServiceFabricNode](./Get-ServiceFabricNode.md)

[Restart-ServiceFabricNode](./Restart-ServiceFabricNode.md)

[Stop-ServiceFabricNode](./Stop-ServiceFabricNode.md)
