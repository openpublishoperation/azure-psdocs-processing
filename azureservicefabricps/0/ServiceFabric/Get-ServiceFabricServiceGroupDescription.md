---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 9226A922-F033-4916-9588-D6BE73ED6F67
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceGroupDescription.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceGroupDescription.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-ServiceFabricServiceGroupDescription

## SYNOPSIS
Gets a Service Fabric service group description.

## SYNTAX

```
Get-ServiceFabricServiceGroupDescription [-ServiceName] <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricServiceGroupDescription** cmdlet gets the Service Fabric service group description of a service that is running. A service group is a group defined by the user. Services that are part of a group would be placed on the same node.

To create a new group use [New-ServiceFabricServiceGroup](./New-ServiceFabricServiceGroup.md) cmdlet.
To update a service group use [Update-ServiceFabricServiceGroup](./Update-ServiceFabricServiceGroup.md) cmdlet.
To remove a service group use [Remove-ServiceFabricServiceGroup](./Remove-ServiceFabricServiceGroup.md) cmdlet.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get a service group description
```
PS C:\>Get-ServiceFabricServiceGroupDescription -ServiceName fabric:/CalcApp/CalcService
```

This command gets the Service Fabric service group description for the service named fabric:/CalcApp/CalcService.


### Example 2: Create, Update and Remove service fabric service groups.
```
PS C:\>New-ServiceFabricServiceGroup -ApplicationName fabric:/myapp/calculator -ServiceName fabric:/myapp/calculator/svc1 -ServiceTypeName StatelessCalculatorService -Stateless -PartitionSchemeSingleton -InstanceCount 3 -ServiceGroupMemberDescription @(@{"ServiceName"="fabric:/myapp/calculator/svc1#a";"ServiceTypeName"="StatelessCalculatorService1"},@{"ServiceName"="fabric:/myapp/calculator/svc1#b";"ServiceTypeName"="StatelessCalculatorService2"})
PS C:\>New-ServiceFabricServiceGroup -ApplicationName fabric:/myapp/calculator -ServiceName fabric:/myapp/calculator/svc1 -ServiceTypeName StatefulCalculatorService -Stateful -TargetReplicaSetSize 5 -MinReplicaSetSize 3 -ReplicaRestartWaitDuration 10 -PlacementConstraint TestPlacementConstraints -ServiceGroupMemberDescription @(@{"ServiceName"="fabric:/myapp/calculator/svc1#a";"ServiceTypeName"="StatelessCalculatorService"})
PS C:\>Get-ServiceFabricServiceGroupDescription -ServiceName fabric:/CalcApp/CalcService
PS C:\>Update-ServiceFabricServiceGroup -ServiceName fabric:/myapp/calculator/svc1 -Stateless -PartitionSchemeSingleton -InstanceCount 3 -ServiceGroupMemberDescription @("fabric:/myapp/calculator/svc1#a,StatelessCalculatorService,")
PS C:\>Remove-ServiceFabricServiceGroup -ServiceName fabric:/myapp/calculator/svc1
```

## PARAMETERS

### -ServiceName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric service group.

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
This cmdlet accepts a URI that represents the name of a Service Fabric service group.

## OUTPUTS

### System.Object
This cmdlet returns a [System.Fabric.Description.ServiceGroupDescription](https://docs.microsoft.com/dotnet/api/system.fabric.description.servicegroupdescription) object for a Service Fabric service group.

## NOTES

## RELATED LINKS

[New-ServiceFabricServiceGroup](./New-ServiceFabricServiceGroup.md)

[Remove-ServiceFabricServiceGroup](./Remove-ServiceFabricServiceGroup.md)

[Update-ServiceFabricServiceGroup](./Update-ServiceFabricServiceGroup.md)
