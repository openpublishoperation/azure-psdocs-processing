---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 9D63C467-E643-4DCD-B8AD-70C741D39377
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationHealth.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationHealth.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricApplicationHealth

## SYNOPSIS
Gets the health of a Service Fabric application.

## SYNTAX

```
Get-ServiceFabricApplicationHealth [-ApplicationName] <Uri> [-ConsiderWarningAsError <Boolean>]
 [-MaxPercentUnhealthyDeployedApplications <Byte>] [-MaxPercentUnhealthyServices <Byte>]
 [-MaxPercentUnhealthyPartitionsPerService <Byte>] [-MaxPercentUnhealthyReplicasPerPartition <Byte>]
 [-EventsHealthStateFilter <Int64>] [-EventsFilter <HealthStateFilter>] [-ServicesHealthStateFilter <Int64>]
 [-ServicesFilter <HealthStateFilter>] [-DeployedApplicationsHealthStateFilter <Int64>]
 [-DeployedApplicationsFilter <HealthStateFilter>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricApplicationHealth** cmdlet gets the health state of a Service Fabric application.
Service Fabric reports the following health states:

- OK.
The entity meets health guidelines.
- Error.
The entity does not meet health guidelines.
- Warning.
The entity meets health guidelines but experienced some issue.

If the entity is not found in the health store, this cmdlet returns an error.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get the health of an application
```
PS C:\>Get-ServiceFabricApplicationHealth -ApplicationName fabric:/myapp/persistenttodolist
```

This command queries the health of the named application.

### Example 2: Get the health of an application using custom health policy and return filters
```
PS C:\>Get-ServiceFabricApplicationHealth -ApplicationName fabric:/myapp/persistenttodolist -ConsiderWarningAsError $True -EventsFilter Error -ServicesFilter 'Error,Warning' -DeployedApplicationsFilter 'Warning,Error'
```

This command queries the health of the named application.
It specifies values for health policy.
It uses filters to return only Error events, and children with Error or Warning health states.

## PARAMETERS

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application.
The cmdlet gets health information for the application that has the URI that you specify.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DeployedApplicationsFilter
Specifies the filter for **DeployedApplicationHealthState** children based on health state.
The value can be obtained from members or bitwise operations on members of **HealthStateFilter**.
Only children that match the filter are returned.
All children are used to evaluate the application aggregated health state.
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

### -DeployedApplicationsHealthStateFilter
This parameter has been deprecated.
Specify the *DeployedApplicationsFilter* parameter instead.

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

### -EventsFilter
Specifies the filter for the collection of **HealthEvent**s reported on the application based on health state.
The value can be obtained from members or bitwise operations on members of **HealthStateFilter**.
Only events that match the filter are returned.
All events are used to evaluate the application aggregated health state.
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

### -MaxPercentUnhealthyDeployedApplications
Specifies the maximum tolerated percentage of unhealthy application instances deployed on the nodes in the cluster.
If there are more deployed applications with health state error than tolerated, the health state of the application is error.
If you do not specify this parameter, the health evaluation uses the value provided in the application manifest.

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

### -MaxPercentUnhealthyPartitionsPerService
Specifies the maximum tolerated percentage of unhealthy service partitions.
If there are more partitions with health state error than tolerated, the health state of the services is error.
If you do not specify this parameter, the health evaluation uses the value provided in the application manifest.

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

### -MaxPercentUnhealthyReplicasPerPartition
Specifies the maximum tolerated percentage of unhealthy partition replicas.
If there are more replicas with health state error than tolerated, the health state of the partition is error.
If you do not specify this parameter, the health evaluation uses the value provided in the application manifest.

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

### -MaxPercentUnhealthyServices
Specifies the maximum tolerated percentage of unhealthy services in an application.
If there are more services with health state error than tolerated, the health state of the application is error.
If you do not specify this parameter, the health evaluation uses the value provided in the application manifest.

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

### -ServicesFilter
Specifies the filter for **ServiceHealthState** children based on health state.
The value can be obtained from members or bitwise operations on members of **HealthStateFilter**.
Only children that match the filter are returned.
All children will be used to evaluate the application aggregated health state.
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

### -ServicesHealthStateFilter
This parameter has been deprecated.
Specify the *ServicesFilter* parameter instead.

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
A URI that represents the name of the Service Fabric application used as filter for the request.

## OUTPUTS

### System.Object
This cmdlet returns an **ApplicationHealth** object that represents the health of the specified Service Fabric application.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
