---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 88E000A6-8A42-4E87-B9E4-7179AC38FB5D
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricPartition.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricPartition.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricPartition

## SYNOPSIS
Gets information about the partitions of a specified Service Fabric partition or service.

## SYNTAX

### QueryByPartitionId (Default)
```
Get-ServiceFabricPartition [-PartitionId] <Guid> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### QueryByServiceName
```
Get-ServiceFabricPartition [[-PartitionId] <Guid>] [-ServiceName] <Uri> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricPartition** cmdlet gets information on the partitions of the specified service or on a specific partition. The returned partition information includes the partition health state, partition status, and service kind (see the [Outputs](#outputs) section for more details).

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the **[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)** cmdlet.

## EXAMPLES

### Example 1: Get partitions for a service
```
PS C:\>Get-ServiceFabricPartition -ServiceName fabric:/myapp/persistenttodolist/svc1
```

This command gets the information for all the partitions of the `fabric:/myapp/persistenttodolist/svc1` service.

### Example 2: Get a specific partition
```
PS C:\>Get-ServiceFabricPartition -PartitionId $ToDoPartition01.PartitionId
```

This command gets the information for the partition stored in the stored in `$ToDoPartition01` object.

## PARAMETERS

### -PartitionId
Specifies the ID of a Service Fabric partition.
If you do not specify this parameter, this cmdlet gets all partitions of the specified service.

```yaml
Type: Guid
Parameter Sets: QueryByPartitionId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: QueryByServiceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifies the URI of a Service Fabric service.

```yaml
Type: Uri
Parameter Sets: QueryByServiceName
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

### System.Uri, System.Guid
This cmdlet accepts a URI that represents the name of a Service Fabric service or a Guid that represents ID of a Service Fabric partition.

## OUTPUTS

### System.Object
This cmdlet returns a list of **[System.Fabric.Query.Partition](https://docs.microsoft.com/dotnet/api/system.fabric.query.partition)** objects that represent Service Fabric partitions.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
