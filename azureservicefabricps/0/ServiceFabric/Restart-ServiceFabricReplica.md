---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 0210C19B-CE2B-4713-9548-515D7DD44BB1
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Restart-ServiceFabricReplica.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Restart-ServiceFabricReplica.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Restart-ServiceFabricReplica

## SYNOPSIS
Restarts a Service Fabric replica to simulate the reopening of a stateful service replica.

## SYNTAX

### ByNodeName
```
Restart-ServiceFabricReplica [-NodeName] <String> [-PartitionId] <Guid> [-ReplicaOrInstanceId] <Int64>
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionIdReplicaId
```
Restart-ServiceFabricReplica [-PartitionId] <Guid> -ServiceName <Uri> [-ReplicaOrInstanceId] <Int64>
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionId
```
Restart-ServiceFabricReplica [-PartitionId] <Guid> -ServiceName <Uri> [-CommandCompletionMode <CompletionMode>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionIdReplicaPrimary
```
Restart-ServiceFabricReplica [-PartitionId] <Guid> -ServiceName <Uri> [-ReplicaKindPrimary]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionIdReplicaRandomSecondary
```
Restart-ServiceFabricReplica [-PartitionId] <Guid> -ServiceName <Uri> [-ReplicaKindRandomSecondary]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionUniformedInt
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindUniformInt64] -PartitionKey <String>
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNameReplicaPrimary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-ReplicaKindPrimary] [-CommandCompletionMode <CompletionMode>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNameReplicaId
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-ReplicaOrInstanceId] <Int64>
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceName
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionSingleton
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindSingleton]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamed
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindNamed] -PartitionKey <String>
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingletonReplicaRandomSecondary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindSingleton] [-ReplicaKindRandomSecondary]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamedReplicaRandomSecondary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindNamed] -PartitionKey <String>
 [-ReplicaKindRandomSecondary] [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionUniformedIntReplicaRandomSecondary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindUniformInt64] -PartitionKey <String>
 [-ReplicaKindRandomSecondary] [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionSingletonReplicaPrimary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindSingleton] [-ReplicaKindPrimary]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamedReplicaPrimary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindNamed] -PartitionKey <String>
 [-ReplicaKindPrimary] [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionUniformedIntReplicaPrimary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindUniformInt64] -PartitionKey <String>
 [-ReplicaKindPrimary] [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingletonReplicaId
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindSingleton] [-ReplicaOrInstanceId] <Int64>
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamedReplicaId
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindNamed] -PartitionKey <String>
 [-ReplicaOrInstanceId] <Int64> [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionUniformedIntReplicaId
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-PartitionKindUniformInt64] -PartitionKey <String>
 [-ReplicaOrInstanceId] <Int64> [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNameReplicaRandomSecondary
```
Restart-ServiceFabricReplica -ServiceName <Uri> [-ReplicaKindRandomSecondary]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Restart-ServiceFabricReplica** cmdlet simulates a service replica failure by restarting a persisted service replica, closing the replica, and then reopening it.
Use this cmdlet to test your service for problems along the replica reopen path.
This cmdlet helps simulate the report fault temporary path through client APIs.
This cmdlet is only valid for replicas that belong to stateful persisted services.

In order to specify the replica to be restarted we can start either with the node name or the service name.

Then we need to specify the partition to which the replica belongs. We can specify the partition either by specifying the pair (naming scheme, partition key) or by specifying the partition ID. For more details on Microsoft Azure Service Fabric service partitioning, please refer to the [Partition Service Fabric reliable services](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-concepts-partitioning) article.  

Lastly, we may need to specify which replica of the partition we are referring to and that can be done either by specifying the replica role (primary or secondary replica) or by specifying the replica ID.

Note, sometimes the user may - instead of exactly specifying the replica - want to restart say one of the secondaries of a particular partition of a particular service; that is why, some of the forms of the Restart-ServiceFabricReplica cmdlet intentionally leaves ambiguity about which replica the user is referring to -- in these cases, the cmdlet makes random choices for the user. For example, if the user only provides the service name to the cmdlet, the Restart-ServiceFabricReplica cmdlet will assume that the user wants to restart any one of the replicas from any one of the partitions belonging to the service; so it will choose one of the partitions of the service at random and will choose one of the replicas (could be primary or secondary) of the chosen partition at random and will restart that chosen replica.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Restart a replica
```
PS C:\>Restart-ServiceFabricReplica -NodeName "Node07" -PartitionId 869dd2e9-fdda-42a5-ad96-4b71c795dfd3 -ReplicaOrInstanceId 12345098480948
```

This command restarts the replica on Node07 on the specified partition.

### Example 2: Restart a primary replica
```
PS C:\>Restart-ServiceFabricReplica -ReplicaKindPrimary -PartitionKindNamed -PartitionKey "Partition1" -ServiceName fabric:/App/Service
```

This command restarts a primary replica on the specified partition.

## PARAMETERS

### -CommandCompletionMode
Specifies whether the action waits for the Restart operation to complete.

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

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet restarts a replica deployed on the node that you specify.

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionId
Specifies the ID of the partition for which to restart the replica.

```yaml
Type: Guid
Parameter Sets: ByNodeName, PartitionIdReplicaId, PartitionId, PartitionIdReplicaPrimary, PartitionIdReplicaRandomSecondary
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKey
Specifies the key of the partition for which the replica is restarted.

```yaml
Type: String
Parameter Sets: ServiceNamePartitionUniformedInt, ServiceNamePartitionNamed, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaRandomSecondary, ServiceNamePartitionNamedReplicaPrimary, ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionNamedReplicaId, ServiceNamePartitionUniformedIntReplicaId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKindNamed
Indicates that this cmdlet restarts a replica on a named partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionNamed, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionNamedReplicaPrimary, ServiceNamePartitionNamedReplicaId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKindSingleton
Indicates that this cmdlet restarts a replica on a singleton partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionSingleton, ServiceNamePartitionSingletonReplicaRandomSecondary, ServiceNamePartitionSingletonReplicaPrimary, ServiceNamePartitionSingletonReplicaId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKindUniformInt64
Indicates that this cmdlet restarts a replica on a UniformInt64 partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionUniformedInt, ServiceNamePartitionUniformedIntReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionUniformedIntReplicaId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplicaKindPrimary
Indicates that this cmdlet restarts the replica for the primary replica.

```yaml
Type: SwitchParameter
Parameter Sets: PartitionIdReplicaPrimary, ServiceNameReplicaPrimary, ServiceNamePartitionSingletonReplicaPrimary, ServiceNamePartitionNamedReplicaPrimary, ServiceNamePartitionUniformedIntReplicaPrimary
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplicaKindRandomSecondary
Indicates that this cmdlet restarts a replica for a random secondary replica.

```yaml
Type: SwitchParameter
Parameter Sets: PartitionIdReplicaRandomSecondary, ServiceNamePartitionSingletonReplicaRandomSecondary, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaRandomSecondary, ServiceNameReplicaRandomSecondary
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplicaOrInstanceId
Specifies a Service Fabric service replica or instance ID.

```yaml
Type: Int64
Parameter Sets: ByNodeName, PartitionIdReplicaId, ServiceNameReplicaId, ServiceNamePartitionSingletonReplicaId, ServiceNamePartitionNamedReplicaId, ServiceNamePartitionUniformedIntReplicaId
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifies the name of a Service Fabric service.

```yaml
Type: Uri
Parameter Sets: PartitionIdReplicaId, PartitionId, PartitionIdReplicaPrimary, PartitionIdReplicaRandomSecondary, ServiceNamePartitionUniformedInt, ServiceNameReplicaPrimary, ServiceNameReplicaId, ServiceName, ServiceNamePartitionSingleton, ServiceNamePartitionNamed, ServiceNamePartitionSingletonReplicaRandomSecondary, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaRandomSecondary, ServiceNamePartitionSingletonReplicaPrimary, ServiceNamePartitionNamedReplicaPrimary, ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionSingletonReplicaId, ServiceNamePartitionNamedReplicaId, ServiceNamePartitionUniformedIntReplicaId, ServiceNameReplicaRandomSecondary
Aliases: 

Required: True
Position: Named
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

### System.Uri
Represents the name of a Service Fabric service.

### System.Guid
Represents the ID of a Service Fabric partition.

### String
Specifies the name of a Service Fabric node.

## OUTPUTS

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricReplica](./Get-ServiceFabricReplica.md)

[Remove-ServiceFabricReplica](./Remove-ServiceFabricReplica.md)
