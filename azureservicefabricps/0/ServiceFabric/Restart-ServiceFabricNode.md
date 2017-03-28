---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 31BD0C1D-F4E0-40B2-B902-06B660D633D9
online version:
schema: 2.0.0
updated_at: Invalid date
ms.date: Invalid date
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Restart-ServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Restart-ServiceFabricNode.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Restart-ServiceFabricNode

## SYNOPSIS
Restarts a Service Fabric node to simulate a cluster node failure.

## SYNTAX

### ByNodeName
```
Restart-ServiceFabricNode [-NodeName] <String> [[-NodeInstanceId] <BigInteger>]
 [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionId
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -PartitionId <Guid>
 -ServiceName <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionIdReplicaRandomSecondary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -PartitionId <Guid>
 -ServiceName <Uri> [-ReplicaKindRandomSecondary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionIdReplicaPrimary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -PartitionId <Guid>
 -ServiceName <Uri> [-ReplicaKindPrimary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### PartitionIdReplicaId
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -PartitionId <Guid>
 -ServiceName <Uri> -ReplicaOrInstanceId <Int64> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamedReplicaId
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindNamed] -PartitionKey <String> -ReplicaOrInstanceId <Int64> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNameReplicaPrimary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-ReplicaKindPrimary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNameReplicaRandomSecondary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-ReplicaKindRandomSecondary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNameReplicaId
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 -ReplicaOrInstanceId <Int64> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingletonReplicaId
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindSingleton] -ReplicaOrInstanceId <Int64> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamed
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindNamed] -PartitionKey <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionUniformedIntReplicaPrimary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindUniformInt64] -PartitionKey <String> [-ReplicaKindPrimary] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionUniformedIntReplicaId
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindUniformInt64] -PartitionKey <String> -ReplicaOrInstanceId <Int64> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceName
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingleton
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindSingleton] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionUniformedInt
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindUniformInt64] -PartitionKey <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingletonReplicaRandomSecondary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindSingleton] [-ReplicaKindRandomSecondary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamedReplicaRandomSecondary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindNamed] -PartitionKey <String> [-ReplicaKindRandomSecondary] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionUniformedIntReplicaRandomSecondary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindUniformInt64] -PartitionKey <String> [-ReplicaKindRandomSecondary] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionSingletonReplicaPrimary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindSingleton] [-ReplicaKindPrimary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamedReplicaPrimary
```
Restart-ServiceFabricNode [-CommandCompletionMode <CompletionMode>] [-CreateFabricDump] -ServiceName <Uri>
 [-PartitionKindNamed] -PartitionKey <String> [-ReplicaKindPrimary] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Restart-ServiceFabricNode** cmdlet restarts a Service Fabric node by restarting the Fabric.exe process that hosts the node.
This cmdlet simulates Service Fabric node failures in the cluster, which tests the failover recovery paths of your service.
For more information, see [Using test actions](https://docs.microsoft.com/azure/service-fabric/service-fabric-testability-actions).

The Service Fabric node to be restarted can specified in the following ways:
- Specify node name and optionally the node instance ID.
- Specify a stateful service replica or stateless service instance and let the cmdlet identify and restart the node that hosts it. The folowing implicit behaviors for replica/instance selection are worth noting:
  - If the service does not use a Singleton partition and neither the **PartitionId** nor **PartitionKey** parameter is specified, then the cmdlet picks a partition randomly.
  - If the service is a stateful service and none of the **Primary**, **RandomSecondary** and **ReplicaOrInstanceId** parameters are specified, then the cmdlet randomly picks a replica, regardless of its role.
  - If the service is a stateless service and the **ReplicaOrInstanceId** parameter is not specified, then the cmdlet randomly picks an instance.

If you specify a non-zero value for the *NodeInstanceId* parameter, that ID is compared with the active node ID.
If the IDs do not match, the process is not restarted and an error occurs.
A stale message can cause this error.

If you specify the *CreateFabricDump* parameter, this cmdlet causes the Fabric.exe process to crash on the specified node during restart.
This crash creates a process dump for Fabric.exe.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Restart a node that hosts a primary replica
```
PS C:\>Restart-ServiceFabricNode -ReplicaKindPrimary -PartitionKindNamed -PartitionKey "Partition3" -CommandCompletionMode Verify
```

This command restarts the node that hosts the primary replica of the partition named Partition3.
Because the *CommandCompletionMode* parameter is specified with a value of Verify, the command waits for the target node to restart before it completes.

### Example 2: Restart a specified node
```
PS C:\>Restart-ServiceFabricNode -NodeName "Node01" -CommandCompletionMode DoNotVerify
```

This command restarts the node named Node01.
Because the *CommandCompletionMode* parameter is specified with a value of DoNotVerify, the command does not wait for the node to restart before it completes.

## PARAMETERS

### -CommandCompletionMode
Specifies whether the action waits for the restart to complete. Specify **Verify** to make the cmdlet wait for restart to complete, and **DoNotVerify** to make the cmdlet return without waiting for restart to complete.

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

### -CreateFabricDump
Indicates that a process dump should be created for Fabric.exe on specified node.

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

### -NodeInstanceId
Specifies a node instance ID.
Unless you specify 0, the node instance ID that you specify must match the currently running node.
To obtain node instance IDs, run [Get-ServiceFabricNode](./Get-ServiceFabricNode.md) for the target node.
For example, for the node N0050, the command `Get-ServiceFabricNode -NodeName "N0050"` returns a [Node](https://docs.microsoft.com/en-us/dotnet/api/system.fabric.query.node) object that contains the node instance ID

```yaml
Type: BigInteger
Parameter Sets: ByNodeName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet restarts the node that you specify.

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
Specifies the partition ID of a Service Fabric service partition. The cmdlet restarts a node that hosts a replica or instance of this partition.

```yaml
Type: Guid
Parameter Sets: PartitionId, PartitionIdReplicaRandomSecondary, PartitionIdReplicaPrimary, PartitionIdReplicaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKey
Specifies a partition key for a Service Fabric service partition. The cmdlet identifies the partition that this partition key maps to and restarts a node that hosts a replica or instance of that partition..

```yaml
Type: String
Parameter Sets: ServiceNamePartitionNamedReplicaId, ServiceNamePartitionNamed, ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionUniformedIntReplicaId, ServiceNamePartitionUniformedInt, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaRandomSecondary, ServiceNamePartitionNamedReplicaPrimary
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKindNamed
Indicates that the **PartitionKey** parameter specifies a partition key for a service that uses Named partitioning scheme.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionNamedReplicaId, ServiceNamePartitionNamed, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionNamedReplicaPrimary
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKindSingleton
Indicates that the service specified in the **ServiceName** parameter uses a Singleton partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionSingletonReplicaId, ServiceNamePartitionSingleton, ServiceNamePartitionSingletonReplicaRandomSecondary, ServiceNamePartitionSingletonReplicaPrimary
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKindUniformInt64
Indicates that the **PartitionKey** parameter specifies a partition key for a service that uses UniformInt64 partitioning scheme.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionUniformedIntReplicaId, ServiceNamePartitionUniformedInt, ServiceNamePartitionUniformedIntReplicaRandomSecondary
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaKindPrimary
Indicates that this cmdlet restarts the node that hosts the primary replica of the specified partition.

```yaml
Type: SwitchParameter
Parameter Sets: PartitionIdReplicaPrimary, ServiceNameReplicaPrimary, ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionSingletonReplicaPrimary, ServiceNamePartitionNamedReplicaPrimary
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaKindRandomSecondary
Indicates that this cmdlet restarts the node that hosts a random secondary replica of the specified partition.

```yaml
Type: SwitchParameter
Parameter Sets: PartitionIdReplicaRandomSecondary, ServiceNameReplicaRandomSecondary, ServiceNamePartitionSingletonReplicaRandomSecondary, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaRandomSecondary
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaOrInstanceId
Specifies a Service Fabric service replica or instance ID. The cmdlet restarts the node that hosts the specified replica or instance.

```yaml
Type: Int64
Parameter Sets: PartitionIdReplicaId, ServiceNamePartitionNamedReplicaId, ServiceNameReplicaId, ServiceNamePartitionSingletonReplicaId, ServiceNamePartitionUniformedIntReplicaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifies the name of a Service Fabric service. The cmdlet restarts a node that hosts a replica or instance of this service.

```yaml
Type: Uri
Parameter Sets: PartitionId, PartitionIdReplicaRandomSecondary, PartitionIdReplicaPrimary, PartitionIdReplicaId, ServiceNamePartitionNamedReplicaId, ServiceNameReplicaPrimary, ServiceNameReplicaRandomSecondary, ServiceNameReplicaId, ServiceNamePartitionSingletonReplicaId, ServiceNamePartitionNamed, ServiceNamePartitionUniformedIntReplicaPrimary, ServiceNamePartitionUniformedIntReplicaId, ServiceName, ServiceNamePartitionSingleton, ServiceNamePartitionUniformedInt, ServiceNamePartitionSingletonReplicaRandomSecondary, ServiceNamePartitionNamedReplicaRandomSecondary, ServiceNamePartitionUniformedIntReplicaRandomSecondary, ServiceNamePartitionSingletonReplicaPrimary, ServiceNamePartitionNamedReplicaPrimary
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

### string
Specifies the name of a Service Fabric node.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Testability.RestartNodeResult** object that represents the operation result.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Disable-ServiceFabricNode](./Disable-ServiceFabricNode.md)

[Enable-ServiceFabricNode](./Enable-ServiceFabricNode.md)

[Get-ServiceFabricNode](./Get-ServiceFabricNode.md)

[Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md)
