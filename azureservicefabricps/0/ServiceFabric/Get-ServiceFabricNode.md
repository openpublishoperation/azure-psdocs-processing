---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 27D58E8F-73CC-4FCE-90BD-449F86127385
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricNode.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-ServiceFabricNode

## SYNOPSIS
Gets information for the all nodes in a Service Fabric cluster or for a specific node.

## SYNTAX

```
Get-ServiceFabricNode [[-NodeName] <String>] [-StatusFilter <NodeStatusFilter>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricNode** cmdlet gets information for all the nodes in a Service Fabric cluster or for a specific node. The returned node information includes the node name, status, type, and health state (see the [Outputs](#outputs) section for more details).

Keep in mind that, before you perform any operation on a Service Fabric cluster you must establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get information for all nodes in the cluster
```
PS C:\>Get-ServiceFabricNode
```

This command returns information for all the nodes in the Service Fabric cluster.

### Example 2: Get information for a specific node
```
PS C:\>Get-ServiceFabricNode -NodeName Node1
```

This command returns information for the node with the name `Node1`.

## PARAMETERS

### -NodeName
Specifies the name of the Service Fabric node whose information is being returned.
If not specified, the cmdlet will return information for all the nodes in the cluster.

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

### -StatusFilter
Specifies the node status filter as a **[System.Fabric.Query.NodeStatusFilter](https://docs.microsoft.com/en-us/dotnet/api/system.fabric.query.nodestatusfilter)** object.

Only nodes with status matching this filter will be returned in the results.

```yaml
Type: NodeStatusFilter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

**Get-ServiceFabricNode** accepts the name of a node as a string.

## OUTPUTS

**Get-ServiceFabricNode** returns instances of the **[System.Fabric.Query.Node](https://docs.microsoft.com/dotnet/api/system.fabric.query.node)**.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Disable-ServiceFabricNode](./Disable-ServiceFabricNode.md)

[Enable-ServiceFabricNode](./Enable-ServiceFabricNode.md)
