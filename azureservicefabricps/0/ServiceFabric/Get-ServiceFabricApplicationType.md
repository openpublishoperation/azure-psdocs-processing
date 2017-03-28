---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 377D093A-8D81-4CDA-842B-EF8A9FF2585C
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationType.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-ServiceFabricApplicationType

## SYNOPSIS
Gets the Service Fabric application types registered on the Service Fabric cluster.

## SYNTAX

```
Get-ServiceFabricApplicationType [[-ApplicationTypeName] <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricApplicationType** cmdlet gets the Service Fabric application types registered on the Service Fabric cluster.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get all registered application types
```
PS C:\>Get-ServiceFabricApplicationType
```

This command gets all registered application types.

### Example 2: Get registered application type with specified type names
```
PS C:\>Get-ServiceFabricApplicationType -ApplicationTypeName "TestApp"
```

This command gets the application types registered with the application type name "TestApp".

## PARAMETERS

### -ApplicationTypeName
Specifies the name of a Service Fabric application type.
The cmdlet gets the application type that you specify.
If you do not specify this parameter, this cmdlet gets all application types.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### String
This cmdlet accepts a string that represents the application type name filter.

## OUTPUTS

### System.Array
An Object[] with each object being a [System.Fabric.Query.ApplicationType](https://msdn.microsoft.com/library/system.fabric.query.applicationtype.aspx) object that represents the Service Fabric application types in case of multiple registered application types.

### System.Object
A [System.Fabric.Query.ApplicationType](https://msdn.microsoft.com/library/system.fabric.query.applicationtype.aspx) object in case of a single registered application type.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Register-ServiceFabricApplicationType](./Register-ServiceFabricApplicationType.md)

[Unregister-ServiceFabricApplicationType](./Unregister-ServiceFabricApplicationType.md)
