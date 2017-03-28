---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 4E889F33-E989-492D-884A-A59A3A89FE08
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Register-ServiceFabricClusterPackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Register-ServiceFabricClusterPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Register-ServiceFabricClusterPackage

## SYNOPSIS
Registers Service Fabric runtime installation file and/or cluster manifest with the cluster.

## SYNTAX

### Both (Default)
```
Register-ServiceFabricClusterPackage -CodePackagePath <String> -ClusterManifestPath <String>
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Code
```
Register-ServiceFabricClusterPackage [-Code] -CodePackagePath <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Config
```
Register-ServiceFabricClusterPackage [-Config] -ClusterManifestPath <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Register-ServiceFabricClusterPackage** cmdlet registers a Service Fabric cluster manifest and/or a Service Fabric runtime installation file.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Register a package that contains both code and configuration
```
PS C:\>Register-ServiceFabricClusterPackage -ClusterManifestPath "ClusterManifest.xml" -CodePackagePath "ServiceFabric.msi"
```

This command registers both the cluster manifest and MSI file with the cluster.

### Example 2: Register only the cluster manifest
```
PS C:\>Register-ServiceFabricClusterPackage -Config -ClusterManifestPath "ClusterManifest.xml"
```

This command registers just the cluster manifest with the cluster.

### Example 3: Register only the runtime installation file
```
PS C:\>Register-ServiceFabricClusterPackage -Code -CodePackagePath "ServiceFabric.msi"
```

This command registers just the runtime installation file with the cluster.

## PARAMETERS

### -ClusterManifestPath
Specifies the path to a Service Fabric cluster manifest file in the ImageStore. This path specified in **ClusterManifestPathInImageStore** in [Copy-ServiceFabricClusterPackage](.\Copy-ServiceFabricClusterPackage.md) cmdlet should be provided here.

```yaml
Type: String
Parameter Sets: Both, Config
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Code
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Code
Specifies that only Service Fabric runtime installation file has to be registered with the cluster.

```yaml
Type: SwitchParameter
Parameter Sets: Code
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CodePackagePath
Specifies the path to a Service Fabric runtime installation file in the ImageStore. This path specified in **CodePackagePathInImageStore** in [Copy-ServiceFabricClusterPackage](.\Copy-ServiceFabricClusterPackage.md) cmdlet should be provided here.

```yaml
Type: String
Parameter Sets: Both, Code
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Config
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Specifies that only Service Fabric cluster manifest file has to be registered with the cluster.

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Copy-ServiceFabricClusterPackage](./Copy-ServiceFabricClusterPackage.md)

[Unregister-ServiceFabricClusterPackage](./Unregister-ServiceFabricClusterPackage.md)
