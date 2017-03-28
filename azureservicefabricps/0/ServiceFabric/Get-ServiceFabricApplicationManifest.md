---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: CF581EAB-D109-4C2A-AD37-A142B63D79FD
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationManifest.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationManifest.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-ServiceFabricApplicationManifest

## SYNOPSIS
Gets the manifest for a Service Fabric application type.

## SYNTAX

```
Get-ServiceFabricApplicationManifest [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricApplicationManifest** cmdlet gets the manifest for a Service Fabric application type.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

To understand the Service Fabric application model, see [Model an application in Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model)

## EXAMPLES

### Example 1: Get an application manifest
```
PS C:\>Get-ServiceFabricApplicationManifest -ApplicationTypeName "PersistentToDoListApp" -ApplicationTypeVersion "1.0"
```

This command gets the application manifest for application type version "1.0" of the application type name "PersistentToDoListApp".

## PARAMETERS

### -ApplicationTypeName
Specifies the name for a Service Fabric application type.
The cmdlet gets the application manifest for the application type name that you specify.

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

### -ApplicationTypeVersion
Specifies the version of a Service Fabric application type.
The cmdlet gets the application manifest for the applicaiton type version that you specify.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### String
This cmdlet accepts a string that represents the application type name or the application type version.

## OUTPUTS

### System.Object
This cmdlet returns a string that represents content from the application manifest.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
