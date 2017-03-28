---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: AC37BE9E-4243-4A85-BC4F-19A56B4FE00B
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceManifest.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceManifest.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-ServiceFabricServiceManifest

## SYNOPSIS
Gets the Service Fabric service type manifest.

## SYNTAX

```
Get-ServiceFabricServiceManifest [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String>
 [-ServiceManifestName] <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricServiceManifest** cmdlet gets the Service Fabric service type manifest. The application containing the service must be registered with [Register-ServiceFabricApplicationType](./Register-ServiceFabricApplicationType.md) before using Get-ServiceFabricServiceManifest.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

To understand the Service Fabric application model, see [Model an application in Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model)

## EXAMPLES

### Example 1: Get the service manifest
```
PS C:\>Get-ServiceFabricServiceManifest -ApplicationTypeName "WordCount" -ApplicationTypeVersion "1.0.0" -ServiceManifestName "WordCountServicePkg"
```

The command gets the service manifest for the service "WordCountServicePkg" of application type "1.0.0" and application version "WordCount".

See [Word Count Sample's Application Manifest](https://github.com/Azure-Samples/service-fabric-dotnet-getting-started/blob/master/Services/WordCount/WordCount/ApplicationPackageRoot/ApplicationManifest.xml)

## PARAMETERS

### -ApplicationTypeName
Specifies the name of a Service Fabric application type. The application type name can be found in the ApplicationManifest.xml.
The cmdlet gets the service manifest for the application type that you specify.

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
Specifies the version of a Service Fabric application type. The application type version can be found in the ApplicationManifest.xml.
The cmdlet gets the service manifest for the application type version that you specify.

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

### -ServiceManifestName
Specifies the name of a Service Fabric service package containing the service manifest. The Service manifest name can be found in the ApplicationManifest.xml.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### String
This cmdlet accepts the name of a Service Fabric application type, the version of this application type and the name of a service package.

## OUTPUTS

### System.Object
This cmdlet returns the content of a Service Fabric service type manifest.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
