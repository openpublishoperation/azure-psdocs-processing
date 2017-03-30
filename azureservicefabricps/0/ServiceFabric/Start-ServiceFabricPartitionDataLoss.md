---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: F83D7B99-CFDC-4A95-A2C7-3CD33925FBAA
online version:
schema: 2.0.0
updated_at: 03/24/2017 15:03 PM
ms.date: 03/24/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricPartitionDataLoss.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricPartitionDataLoss.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/bc0ec5bc26f85fe1bd8f50fdd7441df1ae0fcddb
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Start-ServiceFabricPartitionDataLoss

## SYNOPSIS
Initiates a data loss fault operation on a partition of a stateful Service Fabric service. For details about how to invoke a data loss operation, see the [Invoke Data Loss](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-use-data-loss-api) article. The various ways to specify or to choose the partition to invoke data loss on are below.

## SYNTAX

### Using PartitionId
```
Start-ServiceFabricPartitionDataLoss -OperationId <Guid> -DataLossMode <DataLossMode> -PartitionId <Guid>
 -ServiceName <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingleton
```
Start-ServiceFabricPartitionDataLoss -OperationId <Guid> -DataLossMode <DataLossMode> -ServiceName <Uri>
 [-PartitionKindSingleton] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamed
```
Start-ServiceFabricPartitionDataLoss -OperationId <Guid> -DataLossMode <DataLossMode> -ServiceName <Uri>
 [-PartitionKindNamed] -PartitionKey <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNameRandomPartition
```
Start-ServiceFabricPartitionDataLoss -OperationId <Guid> -DataLossMode <DataLossMode> -ServiceName <Uri>
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionUniformedInt
```
Start-ServiceFabricPartitionDataLoss -OperationId <Guid> -DataLossMode <DataLossMode> -ServiceName <Uri>
 [-PartitionKindUniformInt64] -PartitionKey <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Start-ServiceFabricPartitionDataLoss** cmdlet initiates a data loss on a stateful service partition in Azure Service Fabric.
To run this cmdlet, **FaultAnalysisService** must be enabled.

Run this cmdlet to perform a data loss fault only for partitions for stateful services.
Do not use this cmdlet to perform a data loss for system services.

You can check the progress of the data loss fault operation using the [Get-ServiceFabricPartitionDataLossProgress](./Get-ServiceFabricPartitionDataLossProgress) cmdlet.

After you invoke **Start-ServiceFabricPartitionDataLoss**, you cannot reverse it.

## EXAMPLES

### Example 1: Start a data loss test for a service by partition ID
```
PS C:\>Start-ServiceFabricPartitionDataLoss -OperationId d3f12b09-6a90-4745-a4fc-3f92149a7419 -DataLossMode FullDataLoss -PartitionId 67e2c139-ccf0-4562-9f2b-bf35e4c2abd4 -ServiceName "fabric:/ContosoApp/ContosoService"
```

This command starts a data loss fault operation for all replicas of the service named fabric:/ContosoApp/ContosoService in the partition that has the ID 67e2c139-ccf0-4562-9f2b-bf35e4c2abd4.
Specify a unique GUID for the *OperationId* parameter.
You can use this ID to check the progress of the data loss fault operation.

## PARAMETERS

### -DataLossMode
Specifies the data loss mode for the data loss fault operation.
The acceptable values for this parameter are:

- PartialDataLoss.
Only a quorum of replicas are removed.
**OnDataLossAsync** is triggered for the partition, but actual data loss depends on the presence of inflight replication.
- FullDataLoss.
All replicas are removed.
All data is lost and **OnDataLossAsync** is triggered.

To find more about **OnDataLossAsync** please refer to the [Back up and restore](https://github.com/Microsoft/azure-docs/blob/master/articles/service-fabric/service-fabric-reliable-services-backup-restore.md) article.

```yaml
Type: DataLossMode
Parameter Sets: (All)
Aliases: 
Accepted values: Invalid, PartialDataLoss, FullDataLoss

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationId
Specifies a unique identifier for this operation.
Specify a unique value.
If you want to check the progress of the fault, you must pass the OperationId that you used for starting the data loss fault into **Get-ServiceFabricPartitionDataLossProgress**.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionId
Specifies the ID of the Service Fabric partition for which this cmdlet starts a data loss fault.

```yaml
Type: Guid
Parameter Sets: PartitionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKey
Specifies the key of the Service Fabric partition for which this cmdlet starts a data loss fault.

```yaml
Type: String
Parameter Sets: ServiceNamePartitionNamed, ServiceNamePartitionUniformedInt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionKindNamed
Indicates that the Service Fabric partition for which this cmdlet starts a data loss fault is a Named partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionNamed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKindSingleton
Indicates that the Service Fabric partition for which this cmdlet starts a data loss fault is a singleton partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionSingleton
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKindUniformInt64
Indicates that the Service Fabric partition for which this cmdlet starts a data loss fault is a UniformInt64 partition.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceNamePartitionUniformedInt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric service.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeoutSec
Specifies the time-out period, in seconds, for the fault.

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

## RELATED LINKS

[Get-ServiceFabricPartitionDataLossProgress](./Get-ServiceFabricPartitionDataLossProgress.md)

[Back up and restore Reliable Services and Reliable Actors](https://github.com/Microsoft/azure-docs/blob/master/articles/service-fabric/service-fabric-reliable-services-backup-restore.md)
