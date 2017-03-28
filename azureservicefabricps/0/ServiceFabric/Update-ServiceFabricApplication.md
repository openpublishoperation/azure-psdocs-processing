---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 38C23E3E-4A54-4C9A-B349-A338006A12DE
online version:
schema: 2.0.0
updated_at: Invalid date
ms.date: Invalid date
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Update-ServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Update-ServiceFabricApplication.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Update-ServiceFabricApplication

## SYNOPSIS
Updates or removes application capacity.

## SYNTAX

```
Update-ServiceFabricApplication [-ApplicationName] <Uri> [-RemoveApplicationCapacity] [-MaximumNodes <Int64>]
 [-MinimumNodes <Int64>] [-Metrics <String[]>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Update-ServiceFabricApplication** cmdlet updates or removes application capacity for an application that has already been created.

Application capacity defines the maximum/minimum nodes for an application, as well as capacity per node for its metrics.

## EXAMPLES

### Example 1: Update MaximumNodes and Metrics
```
PS C:\>Update-ServiceFabricApplication fabric:/MyApp -MaximumNodes 6 -Metrics @("CPU,2,12,16")
```

This command updates the application fabric:/MyApp to use a maximum of six nodes.
Each node has a reserved load of two units, and a maximum load of 12 units for the CPU metric on each node.
The total application capacity is 16 units for the CPU metric.
The value for *MinimumNodes* remains unchanged.

### Example 2: Update MaximumNodes and reset metrics
```
PS C:\>Update-ServiceFabricApplication fabric:/MyApp -MaximumNodes 6 -Metrics @()
```

This command updates the application fabric:/MyApp to use a maximum of six nodes, and removes capacities for all metrics.
If there are any previously defined capacities, they are cleared after this command.
The value for *MinimumNodes* is unchanged.

### Example 3: Update all application capacity parameters
```
PS C:\>Update-ServiceFabricApplication fabric:/MyApp -MinumumNodes 2 -MaximumNodes 6 -Metrics @("CPU,2,12,16")
```

This command updates the application fabric:/MyApp to use a maximum of six nodes.
Each node has a reserved load of two units and a maximum load of 12 units for the metric CPU on each node.
The total application capacity is 16 units for the CPU metric.
The value for minimum nodes is updated to 2, so that Service Fabric reserves a total capacity of four units for the CPU metric in the cluster.

### Example 4: Remove all application capacity parameters
```
PS C:\>Update-ServiceFabricApplication fabric:/MyApp -RemoveApplicationCapacity
```

This command updates the application fabric:/MyApp so that it does not have any application capacity parameters defined.
If MyApp had any previously set capacity parameters, this operation clears them.

## PARAMETERS

### -ApplicationName
Specifies the name of the application to update.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumNodes
Specifies the maximum number of nodes on which to place an application.
The value of this parameter must be a non-negative integer.
The default value is 0, which indicates the application can be placed on any number of nodes in the cluster.

If you don't specify this parameter, the application uses the existing maximum number of nodes set for the application.

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

### -Metrics
Specifies an array of metrics. These metrics are used by Service Fabric Cluster Resource Manager to manage resources in the cluster. For more information about metrics and resource managent in Service Fabric, see [Service Fabric Cluster Resource Manager Introduction](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction).
Each metric can follow the pattern MetricName,NodeReservationCapacity,MaximumNodeCapacity,TotalApplicationCapacity, or can specify MetricName and use parameter names NodeReservationCapacity,MaximumNodeCapacity,TotalApplicationCapacity followed by a parameter value separated with a colon.
Each parameter **name:value** pair can appear at most once.

- MetricName.
Specifies the name of the metric.
- NodeReservationCapacity.
Specifies the amount of metric load that is reserved on nodes that have instances of this application.
If *MinimumNodes* is specified, the product of these values is the capacity reserved in the cluster for the application.
- MaximumNodeCapacity.
Specifies the maximum load for an instance of this application on a single node.
Even if the capacity of the node is greater than this value, Service Fabric limits the total load of the application's child replicas to this value.
- TotalApplicationCapacity.
Specifies the total capacity for the application in the cluster.
Service Fabric attempts to limit the sum of loads of the application's child replicas to this value.

While updating capacity, Service Fabric performs the following validations and will fail the command if they do not pass:

- NodeReservationCapacity must not be more than MaximumNodeCapacity.
- If both the *MinimumNodes* parameter and NodeReservationCapacity metric are specified, then the product of *MinimumNodes* and NodeReservationCapacity must not be more than TotalApplicationCapacity.

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

### -MinimumNodes
Specifies the number of nodes in a cluster on which capacity is reserved for this application, this does not mean that the application is guaranteed to have replicas on all those nodes.
The value of this parameter must be a non-negative integer. Default value for this is zero which means no capacity is reserved for the application.

If MinimumNodes is set to 0, no capacity is reserved.

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

### -RemoveApplicationCapacity
Indicates that this operation clears all parameters related to application capacity for the application.
If you specify this parameter, you cannot specify the *Metrics* parameter to update application capacity.

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

###  
None.

## OUTPUTS

###  
None.

## NOTES

## RELATED LINKS

[Get-ServiceFabricApplication](./Get-ServiceFabricApplication.md)

[New-ServiceFabricApplication](./New-ServiceFabricApplication.md)

[Remove-ServiceFabricApplication](./Remove-ServiceFabricApplication.md)

[Test-ServiceFabricApplication](./Test-ServiceFabricApplication.md)
