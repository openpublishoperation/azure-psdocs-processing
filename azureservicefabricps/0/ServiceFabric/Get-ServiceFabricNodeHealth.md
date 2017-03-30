---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 7F34631C-B8A8-4625-96BE-4972166A4EA0
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricNodeHealth.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricNodeHealth.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricNodeHealth

## SYNOPSIS
Gets the health state of a Service Fabric node.

## SYNTAX

```
Get-ServiceFabricNodeHealth [-NodeName] <String> [-ConsiderWarningAsError <Boolean>]
 [-MaxPercentUnhealthyNodes <Byte>] [-EventsHealthStateFilter <Int64>] [-EventsFilter <HealthStateFilter>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricNodeHealth** cmdlet gets the health of a Service Fabric node.
If the node that you specify by name does not exist in the health store, this cmdlet returns an error.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get health of a cluster node
```
PS C:\>Get-ServiceFabricNodeHealth -NodeName "Node01"
```

This command gets the health events reported for the node named Node01.

### Example 2: Get the health of a cluster node using custom health policy and return filters
```
PS C:\>Get-ServiceFabricNodeHealth -NodeName "Node01" -ConsiderWarningAsError $True -EventsFilter Error
```

This command queries the health of the cluster node named Node01.
It specifies values for health policy.
It uses filters to return only Error events.

## PARAMETERS

### -ConsiderWarningAsError
Indicates whether to treat a warning health report as error during health evaluation.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventsFilter
Specifies the filter for the collection of **HealthEvent**s reported on the node based on health state.
The value can be obtained from members or bitwise operations on members of **HealthStateFilter**.
Only events that match the filter are returned.
All events are used to evaluate the node aggregated health state.
If not specified, all entries are returned.

```yaml
Type: HealthStateFilter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventsHealthStateFilter
This parameter has been deprecated.
Specify the *EventsFilter* parameter instead.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPercentUnhealthyNodes
Specifies the maximum tolerated percentage of unhealthy nodes.
If there are more nodes with health state error than tolerated, the cluster is evaluated as error.

Do not specify this parameter.

```yaml
Type: Byte
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet gets health for the node that you specify.

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

### String
This cmdlet accepts the name of a Service Fabric node.

## OUTPUTS

### System.Fabric.Health.NodeHealth
This cmdlet returns a **NodeHealth** object that represents the health of a Service Fabric node.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
