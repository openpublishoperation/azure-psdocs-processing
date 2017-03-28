---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: FD4821A9-3C2A-4AFB-9611-D46FF1D4772C
online version:
schema: 2.0.0
updated_at: Invalid date
ms.date: Invalid date
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricClusterManifest.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricClusterManifest.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Test-ServiceFabricClusterManifest

## SYNOPSIS
Validates a Service Fabric cluster manifest.

## SYNTAX

```
Test-ServiceFabricClusterManifest [-ClusterManifestPath] <String> [-OldClusterManifestPath <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Test-ServiceFabricClusterManifest** cmdlet validates a Service Fabric cluster manifest.
In order to help avoid issues with new Service Fabric cluster deployments or cluster upgrades, we recommended that you test the cluster manifest for obvious errors.
This cmdlet does not discover issues with configuration values.

## EXAMPLES

### Example 1: Validate a cluster manifest
```
PS C:\>Test-ServiceFabricClusterManifest -ClusterManifestPath \\configStore\ClusterManifests\CH1\ClusterManifest_123.xml
```

This command validates the specified Service Fabric cluster manifest.

### Example 2: Validate an updated cluster manifest
```
PS C:\>Test-ServiceFabricClusterManifest -ClusterManifestPath \\configStore\ClusterManifests\CH1\ClusterManifest_123.v2.xml -OldClusterManifestPath \\configStore\ClusterManifests\CH1\ClusterManifest_123.v1.xml
```

This command validates the specified cluster manifest against an existing cluster manifest file. This is helpful for validating the changes between the two cluster manifests and catching potential errors before starting a cluster upgrade.

## PARAMETERS

### -ClusterManifestPath
Specifies the path to a Service Fabric cluster manifest.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OldClusterManifestPath
Specifies the path of an existing Service Fabric cluster manifest that is already deployed.
The cmdlet validates the manifest specified in **ClusterManifestPath** against the manifest that this parameter specifies for configuration upgrade purposes.

```yaml
Type: String
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

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns $True if the Service Fabric cluster manifest is valid, or, if it is not valid, this cmdlet returns $False.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricClusterManifest](./Get-ServiceFabricClusterManifest.md)
