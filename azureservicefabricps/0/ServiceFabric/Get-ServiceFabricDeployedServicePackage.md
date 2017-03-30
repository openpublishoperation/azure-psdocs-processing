---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 623857D1-E8E9-43D9-A4BD-20F97F4C9B37
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricDeployedServicePackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricDeployedServicePackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricDeployedServicePackage

## SYNOPSIS
Gets the Service Fabric service packages on a node.

## SYNTAX

```
Get-ServiceFabricDeployedServicePackage [-NodeName] <String> [-ApplicationName] <Uri>
 [[-ServiceManifestName] <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricDeployedServicePackage** cmdlet gets the Service Fabric deployed service packages on a specified node.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get all deployed service packages
```
PS C:\>Get-ServiceFabricDeployedServicePackage -NodeName "Node01" -ApplicationName fabric:/MyApplication
```

This command gets all deployed service packages for application fabric:/MyApplication on node Node01.

### Example 2: Get deployed service package for service manifest
```
PS C:\>Get-ServiceFabric DeployedServicePackage -NodeName "Node01" -ApplicationName fabric:/MyApplication -ServiceManifestName "CalcServicePackage"
```

This command gets deployed service package for application fabric:/MyApplication on node Node01 for service manifest CalcServicePackage.

## PARAMETERS

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application.
The cmdlet gets the service package for the application that you specify.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet gets service packages for the node that you specify.

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

### -ServiceManifestName
Specifies the name of a Service Fabric service manifest.
The cmdlet gets service packages for the service manifest that you specify.

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

### System.Uri, String
This cmdlet accepts a URI that represents the name of a Service Fabric application, or a Service Fabric node name, or a service name.

## OUTPUTS

### System.Object
This cmdlet returns **DeployedServicePackage** objects that represent service packages.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricService](./Get-ServiceFabricService.md)
