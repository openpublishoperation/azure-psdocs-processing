---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: D772E7FA-EA9A-494A-913F-584F9891F880
online version:
schema: 2.0.0
updated_at: 03/23/2017 20:03 PM
ms.date: 03/23/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Invoke-ServiceFabricPartitionDataLoss.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Invoke-ServiceFabricPartitionDataLoss.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/fac2031a80184883cdb99fa4a8c6e1971ab6aaf2
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Invoke-ServiceFabricPartitionDataLoss

## SYNOPSIS
**DEPRECATED**. Please use the [Start-ServiceFabricPartitionDataLoss](./Start-ServiceFabricPartitionDataLoss.md).

## SYNTAX

### PartitionId
```
Invoke-ServiceFabricPartitionDataLoss -DataLossMode <DataLossMode> -PartitionId <Guid> -ServiceName <Uri>
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionSingleton
```
Invoke-ServiceFabricPartitionDataLoss -DataLossMode <DataLossMode> -ServiceName <Uri> [-PartitionKindSingleton]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNamePartitionNamed
```
Invoke-ServiceFabricPartitionDataLoss -DataLossMode <DataLossMode> -ServiceName <Uri> [-PartitionKindNamed]
 -PartitionKey <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### ServiceNameRandomPartition
```
Invoke-ServiceFabricPartitionDataLoss -DataLossMode <DataLossMode> -ServiceName <Uri> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

### ServiceNamePartitionUniformedInt
```
Invoke-ServiceFabricPartitionDataLoss -DataLossMode <DataLossMode> -ServiceName <Uri>
 [-PartitionKindUniformInt64] -PartitionKey <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-ServiceFabricPartitionDataLoss** cmdlet induces data loss in a specified Service Fabric partition to test the data recovery path for a service.

## PARAMETERS

### -DataLossMode
Specifies the data loss mode for the operation.
The acceptable values for this parameter are:

- PartialDataLoss
- FullDataLoss

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

### -PartitionId
Specifies the ID of the partition on which to invoke the data loss.

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
Specifies the key of the partition on which to invoke the test.

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
Indicates that this cmdlet invokes data loss on a named partition.

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
Indicates that this cmdlet invokes data loss on a singleton partition.

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
Indicates that this cmdlet invokes data loss on a UniformInt64 partitioned service.

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
Specifies the name of the service to test.

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

### System.Guid
Represents the ID of a Service Fabric partition.

### System.Uri
Represents the name of a Service Fabric service.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Testability.InvokeDataLossResult** object that represents the operation result.

## RELATED LINKS

[Invoke-ServiceFabricPartitionQuorumLoss](./Invoke-ServiceFabricPartitionQuorumLoss.md)

[Remove-ServiceFabricTestState](./Remove-ServiceFabricTestState.md)
