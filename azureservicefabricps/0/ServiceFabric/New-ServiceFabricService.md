---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 3C647305-B5A8-4CB7-8655-CC7695736CE0
online version:
schema: 2.0.0
updated_at: Invalid date
ms.date: Invalid date
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/New-ServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/New-ServiceFabricService.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# New-ServiceFabricService

## SYNOPSIS
Creates a Service Fabric service.

## SYNTAX

### Stateless Singleton Non-Adhoc (Default)
```
New-ServiceFabricService [-Stateless] [-PartitionSchemeSingleton] [-ApplicationName] <Uri> [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -InstanceCount <Int32> [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateful UniformInt64 Adhoc
```
New-ServiceFabricService [-Stateful] [-PartitionSchemeUniformInt64] [-Adhoc] [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -PartitionCount <Int32> -LowKey <Int64> -HighKey <Int64> [-HasPersistedState]
 -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32> [-ReplicaRestartWaitDuration <TimeSpan>]
 [-QuorumLossWaitDuration <TimeSpan>] [-StandByReplicaKeepDuration <TimeSpan>] [-PlacementConstraint <String>]
 [-Metric <String[]>] [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Stateful UniformInt64 Non-Adhoc
```
New-ServiceFabricService [-Stateful] [-PartitionSchemeUniformInt64] [-ApplicationName] <Uri>
 [-ServiceName] <Uri> [-ServiceTypeName] <String> -PartitionCount <Int32> -LowKey <Int64> -HighKey <Int64>
 [-HasPersistedState] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateful Named Non-Adhoc
```
New-ServiceFabricService [-Stateful] [-PartitionSchemeNamed] [-ApplicationName] <Uri> [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -PartitionNames <String[]> [-HasPersistedState] -TargetReplicaSetSize <Int32>
 -MinReplicaSetSize <Int32> [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateful Singleton Adhoc
```
New-ServiceFabricService [-Stateful] [-PartitionSchemeSingleton] [-Adhoc] [-ServiceName] <Uri>
 [-ServiceTypeName] <String> [-HasPersistedState] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateful Singleton Non-Adhoc
```
New-ServiceFabricService [-Stateful] [-PartitionSchemeSingleton] [-ApplicationName] <Uri> [-ServiceName] <Uri>
 [-ServiceTypeName] <String> [-HasPersistedState] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateful Named Adhoc
```
New-ServiceFabricService [-Stateful] [-PartitionSchemeNamed] [-Adhoc] [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -PartitionNames <String[]> [-HasPersistedState] -TargetReplicaSetSize <Int32>
 -MinReplicaSetSize <Int32> [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateless Singleton Adhoc
```
New-ServiceFabricService [-Stateless] [-PartitionSchemeSingleton] [-Adhoc] [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -InstanceCount <Int32> [-PlacementConstraint <String>] [-Metric <String[]>]
 [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### Stateless Named Adhoc
```
New-ServiceFabricService [-Stateless] [-PartitionSchemeNamed] [-Adhoc] [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -PartitionNames <String[]> -InstanceCount <Int32> [-PlacementConstraint <String>]
 [-Metric <String[]>] [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Stateless UniformInt64 Non-Adhoc
```
New-ServiceFabricService [-Stateless] [-PartitionSchemeUniformInt64] [-ApplicationName] <Uri>
 [-ServiceName] <Uri> [-ServiceTypeName] <String> -PartitionCount <Int32> -LowKey <Int64> -HighKey <Int64>
 -InstanceCount <Int32> [-PlacementConstraint <String>] [-Metric <String[]>] [-Correlation <String[]>]
 [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Stateless Named Non-Adhoc
```
New-ServiceFabricService [-Stateless] [-PartitionSchemeNamed] [-ApplicationName] <Uri> [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -PartitionNames <String[]> -InstanceCount <Int32> [-PlacementConstraint <String>]
 [-Metric <String[]>] [-Correlation <String[]>] [-PlacementPolicy <String[]>] [-DefaultMoveCost <String>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Stateless UniformInt64 Adhoc
```
New-ServiceFabricService [-Stateless] [-PartitionSchemeUniformInt64] [-Adhoc] [-ServiceName] <Uri>
 [-ServiceTypeName] <String> -PartitionCount <Int32> -LowKey <Int64> -HighKey <Int64> -InstanceCount <Int32>
 [-PlacementConstraint <String>] [-Metric <String[]>] [-Correlation <String[]>] [-PlacementPolicy <String[]>]
 [-DefaultMoveCost <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **New-ServiceFabricService** cmdlet creates a Service Fabric service.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

Before performing this operation, please upload application package, register application type, and create application instance first. For more information, see [Deploy and remove applications using PowerShell](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-remove-applications).

To get the services created under an application, use [Get-ServiceFabricService](./Get-ServiceFabricService.md).

## EXAMPLES

### Example 1: Create a stateless service by using a singleton partitioning scheme.
```
PS C:\>New-ServiceFabricService -ApplicationName fabric:/HelloWorld -ServiceName fabric:/HelloWorld/svc1 -ServiceTypeName HelloWorldStateless -Stateless -PartitionSchemeSingleton -InstanceCount -1
```

This command creates a Service Fabric stateless service from the specified application instance by using a singleton partitioning scheme.

### Example 2: Create a stateful service by using a singleton partitioning scheme.
```
PS C:\>New-ServiceFabricService -ApplicationName fabric:/HelloWorld -ServiceName fabric:/HelloWorld/svc1 -ServiceTypeName HelloWorldStateful -Stateful -PartitionSchemeSingleton -TargetReplicaSetSize 3 -MinReplicaSetSize 2
```

This command creates a Service Fabric stateful service from the specified application instance by using a singleton partitioning scheme.

### Example 3: Create a stateless service by using ranged partitioning sheme.
```
New-ServiceFabricService -ApplicationName fabric:/HelloWorld -ServiceName fabric:/HelloWorld/svc1 -ServiceTypeName HelloWorldStateless -Stateless -PartitionSchemeUniformInt64 -PartitionCount 26 -LowKey 0 -HighKey 51 -InstanceCount -1
```

This command creates a Service Fabric stateless service from the specified application instance with ranged partitioning scheme.

### Example 4: Create a stateless service by using named partitioning sheme.
```
New-ServiceFabricService -ApplicationName fabric:/HelloWorld -ServiceName fabric:/HelloWorld/svc1 -ServiceTypeName HelloWorldStateless -Stateless -PartitionSchemeNamed -PartitionNames @("Seattle","Vancouver") -InstanceCount -1
```

This command creates a Service Fabric stateless service from the specified application instance with named partitioning scheme.

### Example 5: Create a stateful service by using ranged partitioning sheme.
```
New-ServiceFabricService -ApplicationName fabric:/HelloWorld -ServiceName fabric:/HelloWorld/svc1 -ServiceTypeName HelloWorldStateful -Stateful -PartitionSchemeUniformInt64 -PartitionCount 26 -LowKey 0 -HighKey 51 -MinReplicaSetSize 2 -TargetReplicaSetSize 3
```

This command creates a Service Fabric stateful service from the specified application instance with ranged partitioning shceme.

### Example 6: Create a stateful service by using named partitioning sheme.
```
New-ServiceFabricService -ApplicationName fabric:/HelloWorld -ServiceName fabric:/HelloWorld/svc1 -ServiceTypeName HelloWorldStateful -Stateful -PartitionSchemeNamed -PartitionNames @("Seattle","Vancouver") -MinReplicaSetSize 2 -TargetReplicaSetSize 3
```

This command creates a Service Fabric stateful service from the specified application instance with named partitioning scheme.

## PARAMETERS

### -Adhoc
Indicates that the service runs in ad hoc mode.
In ad hoc mode, the service host is manually activated.
Note: This is only for legacy support.

```yaml
Type: SwitchParameter
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful Singleton Adhoc, Stateful Named Adhoc, Stateless Singleton Adhoc, Stateless Named Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application.
This is the unique name of an application and is used to group services together for management. The scheme must be "fabric:/" and the service name must start with the application name.
The cmdlet creates a service based on this application.

```yaml
Type: Uri
Parameter Sets: Stateless Singleton Non-Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Non-Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless Named Non-Adhoc
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Correlation
Correlation is a control that is provided mainly to help ease the transition of larger monolithic applications into the cloud and microservices world.
For more information, see [Managing resource consumption and load in Service Fabric with metrics](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-advanced-placement-rules-affinity).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultMoveCost
The default cost for a move.
Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster.
Valid values are:

- Zero
- Low
- Medium
- High

For more information, see [Managing resource consumption and load in Service Fabric with metrics](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-movement-cost).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HasPersistedState
Indicates that the stateful service has persistent state.
When a FabricReplicator at a secondary replica receives an operation for a persistent service, it must wait for the service to acknowledge that the data has been persisted before it can send that acknowledgment back to the primary. For non-persistent services, the operation can be acknowledged immediately upon receipt.

```yaml
Type: SwitchParameter
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HighKey
Specifies the high key range of the partition set.

```yaml
Type: Int64
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Specifies the number of instances that the system creates and maintains for each partition of this Service Fabric stateless service.
Setting InstanceCount to -1 implies deploying instances to all the nodes within the cluster.

```yaml
Type: Int32
Parameter Sets: Stateless Singleton Non-Adhoc, Stateless Singleton Adhoc, Stateless Named Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless Named Non-Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LowKey
Specifies the low key range of the partition set.

```yaml
Type: Int64
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metric
Metrics are the set of resources that a given named service instance needs. A service's metric configuration includes how much of that resource each stateful replica or stateless instance of that service consumes by default. Metrics also include a weight that indicates how important balancing that metric is to that service, in case tradeoffs are necessary.

For more information, see [Managing resource consumption and load in Service Fabric with metrics](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-metrics).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinReplicaSetSize
Specifies the minimum replica set size that Service Fabric will keep in its view of the Replica Set for a given partition.

```yaml
Type: Int32
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionCount
Specifies the number of partitions for the Service Fabric service.

```yaml
Type: Int32
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionNames
Specifies an array of names of partitions.

```yaml
Type: String[]
Parameter Sets: Stateful Named Non-Adhoc, Stateful Named Adhoc, Stateless Named Adhoc, Stateless Named Non-Adhoc
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionSchemeNamed
Indicates that the service uses the named partition scheme.
Services using this model usually have data that can be bucketed, within a bounded set. Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.

```yaml
Type: SwitchParameter
Parameter Sets: Stateful Named Non-Adhoc, Stateful Named Adhoc, Stateless Named Adhoc, Stateless Named Non-Adhoc
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionSchemeSingleton
Indicates that the service uses the singleton partition scheme.
Singleton partitions are typically used when the service does not require any additional routing.

```yaml
Type: SwitchParameter
Parameter Sets: Stateless Singleton Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateless Singleton Adhoc
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionSchemeUniformInt64
Indicates that the service uses the UniformInt64 partition scheme. This means that each partition owns a range of int64 keys.

```yaml
Type: SwitchParameter
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlacementConstraint
Placement Constraints are Boolean statements which allow services to select for particular node properties (and the values of those properties) in order to control where it is legal to place them.
For more information, see [Placement constraints and node properties](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description#placement-constraints-and-node-properties).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlacementPolicy
Placement Policies are used to for a given service to always run or never run in certain regions, similarly to try to place the Primary in a certain region to minimize end-user latency.
For more information, see [Placement policies for service fabric services](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-advanced-placement-rules-placement-policies).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QuorumLossWaitDuration
Specifies the duration, as a **TimeSpan** object, that Service Fabric waits before it declares data loss for the service partition.
To obtain a **TimeSpan** object, use the [New-TimeSpan](http://go.microsoft.com/fwlink/?LinkID=113360) cmdlet.
For more information, type `Get-Help New-TimeSpan`.

```yaml
Type: TimeSpan
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaRestartWaitDuration
Specifies the interval, as a **TimeSpan** object, that Service Fabric waits for a replica to restart before it starts building a replacement replica.
To obtain a **TimeSpan** object, use the [New-TimeSpan](http://go.microsoft.com/fwlink/?LinkID=113360) cmdlet.

```yaml
Type: TimeSpan
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifies the URI of a Service Fabric service.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTypeName
Specifies the name of a Service Fabric service type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandByReplicaKeepDuration
Specifies the duration, as a **TimeSpan** object, that a replica with persistent state remains in the replica set even if it has already been replaced, that is, when the target replica set size is already satisfied.
To obtain a **TimeSpan** object, use the [New-TimeSpan](http://go.microsoft.com/fwlink/?LinkID=113360) cmdlet.

```yaml
Type: TimeSpan
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stateful
Indicates that the service is a Service Fabric stateful service.

```yaml
Type: SwitchParameter
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Stateless
Indicates that the service is a Service Fabric stateless service.

```yaml
Type: SwitchParameter
Parameter Sets: Stateless Singleton Non-Adhoc, Stateless Singleton Adhoc, Stateless Named Adhoc, Stateless UniformInt64 Non-Adhoc, Stateless Named Non-Adhoc, Stateless UniformInt64 Adhoc
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetReplicaSetSize
Specifies the number of replicas that the system creates and maintains for each partition of this Service Fabric stateful service.

```yaml
Type: Int32
Parameter Sets: Stateful UniformInt64 Adhoc, Stateful UniformInt64 Non-Adhoc, Stateful Named Non-Adhoc, Stateful Singleton Adhoc, Stateful Singleton Non-Adhoc, Stateful Named Adhoc
Aliases: 

Required: True
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

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Description.ServiceDescription** object for the Service Fabric service.

## NOTES

## RELATED LINKS

[New-TimeSpan](http://go.microsoft.com/fwlink/?LinkID=113360)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricService](./Get-ServiceFabricService.md)

[Remove-ServiceFabricService](./Remove-ServiceFabricService.md)

[Resolve-ServiceFabricService](./Resolve-ServiceFabricService.md)

[Update-ServiceFabricService](./Update-ServiceFabricService.md)
