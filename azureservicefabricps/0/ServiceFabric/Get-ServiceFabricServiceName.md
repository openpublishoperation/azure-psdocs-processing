---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceName.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceName.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricServiceName

## SYNOPSIS
Gets the name of the service for a Service Fabric partition.

## SYNTAX

```
Get-ServiceFabricServiceName [-PartitionId] <Guid> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricServiceName** cmdlet gets the name of the service for a Service Fabric partition.

The output of **Get-ServiceFabricServiceName** contains the following information:

--Service Name: The name of the service corresponding to the given partition.

## EXAMPLES

### Example 1: Get the service name for a partition
```
PS C:\> Get-ServiceFabricServiceName -PartitionId $ToDoPartition01.PartitionId
```

This command gets the name of the service by using the PartitionId property of the object stored in $ToDoPartition01.

### Example 2: Restart the replica for a partition
```
PS C:\> Get-ServiceFabricServiceName -PartitionId $ToDoPartition01.PartitionId | Restart-ServiceFabricReplica
```

The **[Restart-ServiceFabricReplica](./Restart-ServiceFabricReplica.md)** cmdlet restarts the replica specified by the given `ServiceName` and `PartitionId`. This example restarts the replica for the `$ToDoPartition01` partition by getting its `ServiceName` using the **Get-ServiceFabricServiceName** cmdlet and piping it, along with its `PartitionId`, to the **Restart-ServiceFabricReplica** cmdlet.

## PARAMETERS

### -PartitionId
Specifies the ID of a Service Fabric partition.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Guid
This cmdlet accepts the ID of a Service Fabric partition.

## OUTPUTS

### System.Object
This cmdlet returns a [System.Fabric.Query.ServiceNameResult](https://docs.microsoft.com/dotnet/api/system.fabric.query.servicenameresult) which represents the service name.

## NOTES

## RELATED LINKS

[Get-ServiceFabricApplicationName](./Get-ServiceFabricApplicationName.md)
