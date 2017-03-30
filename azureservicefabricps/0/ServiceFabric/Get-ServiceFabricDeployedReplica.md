---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: DFC277E2-C2C5-451D-9029-0D9054A53E82
online version:
schema: 2.0.0
updated_at: 03/09/2017 17:03 PM
ms.date: 03/09/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricDeployedReplica.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricDeployedReplica.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/693945a72fd0a71cabe7aa5cb9e51c0b8d12af11
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricDeployedReplica

## SYNOPSIS
Gets information about a Service Fabric replica on a node. 

## SYNTAX

### Non-Adhoc (Default)
```
Get-ServiceFabricDeployedReplica [-NodeName] <String> [-ApplicationName] <Uri>
 [[-ServiceManifestName] <String>] [[-PartitionId] <Guid>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Adhoc
```
Get-ServiceFabricDeployedReplica [-NodeName] <String> [-Adhoc] [[-ServiceManifestName] <String>]
 [[-PartitionId] <Guid>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricDeployedReplica** cmdlet gets information about a Service Fabric replica running on a node. This provides additional information such as the name of the code package hosting the replica that is not available from [Get-ServiceFabricReplica](./Get-ServiceFabricReplica.md)

This information may be different from the information returned by the [Get-ServiceFabricReplica](./Get-ServiceFabricReplica.md) cmdlet because the node has the most current view of the replica.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get all deployed replicas
```
PS C:\>Get-ServiceFabricDeployedReplica -NodeName "Node01" -ApplicationName fabric:/MyApplication
```

This command gets all deployed replicas for application fabric:/MyApplication on node Node01.

## PARAMETERS

### -Adhoc
Indicates that the service runs in ad hoc mode.
In ad hoc mode, you manually activate the service host.

```yaml
Type: SwitchParameter
Parameter Sets: Adhoc
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application.
The cmdlet gets the information about replicas of the application that has the URI that you specify.

```yaml
Type: Uri
Parameter Sets: Non-Adhoc
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet gets the information of the replicas running on the node that you specify.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartitionId
Specifies the ID of a Service Fabric partition.
This is an additional filter to return the replica that belongs to a specific partition.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceManifestName
Specifies the name of a Service Fabric service manifest in the application specified by the *ApplicationName* parameter.
This parameter can be used to filter to only replicas in a specific service manifest.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### System.Uri, System.Guid, String
This cmdlet accepts a URI that represents the name of a Service Fabric application, or a string that represents a Service Fabric node name where replicas are deployed, or a GUID of a Service Fabric partition filter, or a string that represents a service manifest name filter.

## OUTPUTS

### System.Object
This cmdlet returns [DeployedServiceReplica](https://docs.microsoft.com/dotnet/api/system.fabric.query.deployedservicereplica) objects that represent the replicas running on the node.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricReplica](./Get-ServiceFabricReplica.md)
