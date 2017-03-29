---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: ED7EBEFF-3AB3-4385-AA3A-AB03870E28EE
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceType.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceType.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricServiceType

## SYNOPSIS
Gets all the Service Fabric service types for the given application type or a specific service type.

## SYNTAX

```
Get-ServiceFabricServiceType [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String>
 [[-ServiceTypeName] <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricServiceType** cmdlet gets all the Service Fabric service types for the given application type, specified by its application type name and application type version, or a specific service type, specified by its application type and service type name.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get the service type information
```
PS C:\>Get-ServiceFabricServiceType -ApplicationTypeName "CalcServiceApp" -ApplicationTypeVersion "1.0"
```

This command gets the information for the service types of version 1.0 of the CalcServiceApp application.

## PARAMETERS

### -ApplicationTypeName
Specifies the name of a Service Fabric application type.
The cmdlet gets the services types for the application type that you specify.

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
The cmdlet gets the service types for the application type version that you specify.

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

### -ServiceTypeName
Specifies the name of a Service Fabric service type.
The cmdlet gets only the service type with the specified service type name.
If not specified, the cmdlet will return all the service types for the given application type.

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

### String
This cmdlet accepts the name of a Service Fabric application type and the version of an application type. A service type name can also be specified to get information for a specific service type.

## OUTPUTS

### System.Object
This cmdlet returns a list of **[System.Fabric.Query.ServiceType](https://docs.microsoft.com/dotnet/api/System.Fabric.Query.ServiceType)** objects that represent Service Fabric service types.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
