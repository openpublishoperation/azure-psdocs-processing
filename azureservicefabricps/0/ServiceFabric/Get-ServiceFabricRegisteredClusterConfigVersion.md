---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: FE81372C-DE58-4921-95AC-35D523C5300D
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricRegisteredClusterConfigVersion.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricRegisteredClusterConfigVersion.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricRegisteredClusterConfigVersion

## SYNOPSIS
Gets provisioned fabric config versions in a Service Fabric cluster.

## SYNTAX

```
Get-ServiceFabricRegisteredClusterConfigVersion [[-ConfigVersion] <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricRegisteredClusterConfigVersion** cmdlet gets provisioned fabric config versions in a Service Fabric cluster.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1:
```
PS C:\>Get-ServiceFabricRegisteredClusterConfigVersion
```

## PARAMETERS

### -ConfigVersion
Specifies a config version.
This cmdlet gets only the provisioned fabric config versions that match the config version that this parameter specifies.

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
This cmdlet accepts the config version of a Service Fabric cluster as a string.

## OUTPUTS

### System.Object
This cmdlet returns a list of [System.Fabric.Query.ProvisionedFabricConfigVersion] (https://docs.microsoft.com/dotnet/api/system.fabric.query.provisionedfabricconfigversion) objects that represents registered Service Fabric cluster config versions.

## NOTES

## RELATED LINKS

[Get-ServiceFabricRegisteredClusterCodeVersion](./Get-ServiceFabricRegisteredClusterCodeVersion.md)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
