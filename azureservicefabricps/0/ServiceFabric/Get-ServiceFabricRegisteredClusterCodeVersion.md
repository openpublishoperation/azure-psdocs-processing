---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: D1A0F338-F89D-40F0-8C1A-AF5453E61092
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricRegisteredClusterCodeVersion.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricRegisteredClusterCodeVersion.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricRegisteredClusterCodeVersion

## SYNOPSIS
Gets all provisioned fabric code versions in a Service Fabric cluster.

## SYNTAX

```
Get-ServiceFabricRegisteredClusterCodeVersion [[-CodeVersion] <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricRegisteredClusterCodeVersion** cmdlet gets provisioned fabric code versions in a Service Fabric cluster.
You can specify a particular code version to get.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1:
```
PS C:\>Get-ServiceFabricRegisteredClusterCodeVersion
```

## PARAMETERS

### -CodeVersion
Specifies a code version.
This cmdlet gets only the provisioned fabric code versions that match the code version that this parameter specifies.

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
This cmdlet accepts the version of a Service Fabric cluster code as a string.

## OUTPUTS

### System.Object
This cmdlet returns a list of [System.Fabric.Query.ProvisionedFabricCodeVersion] (https://docs.microsoft.com/dotnet/api/system.fabric.query.provisionedfabriccodeversion) objects that represent registered cluster code versions.

## NOTES

## RELATED LINKS

[Get-ServiceFabricRegisteredClusterConfigVersion](./Get-ServiceFabricRegisteredClusterConfigVersion.md)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
