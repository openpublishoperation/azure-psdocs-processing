---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 6DB6444E-9271-42D4-8EC9-73CA6A799369
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Copy-ServiceFabricClusterPackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Copy-ServiceFabricClusterPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Copy-ServiceFabricClusterPackage

## SYNOPSIS
Copies a Service Fabric runtime installation file and/or cluster manifest to the image store.

## SYNTAX

### Both (Default)
```
Copy-ServiceFabricClusterPackage -CodePackagePath <String> -ClusterManifestPath <String>
 -ImageStoreConnectionString <String> [-CodePackagePathInImageStore <String>]
 [-ClusterManifestPathInImageStore <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Code
```
Copy-ServiceFabricClusterPackage [-Code] -CodePackagePath <String> -ImageStoreConnectionString <String> [-CodePackagePathInImageStore <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Config
```
Copy-ServiceFabricClusterPackage [-Config] -ClusterManifestPath <String> -ImageStoreConnectionString <String> [-ClusterManifestPathInImageStore <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Copy-ServiceFabricClusterPackage** cmdlet copies a Service Fabric runtime installation file and/or cluster manifest to the image store.

After copying the package to the image store, use the [Register-ServiceFabricClusterPackage](.\Register-ServiceFabricClusterPackage.md) cmdlet to register the package.

After registering the package to the image store, use the [Remove-ServiceFabricClusterPackage](.\Remove-ServiceFabricClusterPackage.md) cmdlet to remove the package from the image store.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](.\Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Copy code and manifest to the image store
```
PS C:\>Copy-ServiceFabricClusterPackage -ClusterManifestPath "\\configStore\ClusterManifests\CH1\ClusterManifest_123.xml" -CodePackagePath "\\codeStore\MsiFiles\ServiceFabric.2.0.59.0.msi" -ImageStoreConnectionString "fabric:ImageStore"
```

This command copies the specified MSI and cluster manifest file to the image store. When **CodePackagePathInImageStore** or **ClusterManifestPathInImageStore** are not provided, the file name will be used by default.

### Example 2: Copy only cluster manifest to the image store
```
PS C:\>Copy-ServiceFabricClusterPackage -Config -ClusterManifestPath "\\configStore\ClusterManifests\CH1\ClusterManifest_123.xml" -ClusterManifestPathInImageStore ClusterManifest.xml -ImageStoreConnectionString "fabric:ImageStore"
```

This command copies the specified cluster manifest to ClusterManifest.xml in the image store.

### Example 3: Copy only runtime installation file to the image store
```
PS C:\>Copy-ServiceFabricClusterPackage -Code -CodePackagePath "\\codeStore\MsiFiles\ServiceFabric.2.0.59.0.msi" -CodePackagePathInImageStore ServiceFabric.msi -ImageStoreConnectionString "fabric:ImageStore"
```

This command copies just the specified MSI file to ServiceFabric.msi in the image store.

## PARAMETERS

### -ClusterManifestPath
Specifies the path to a Service Fabric cluster manifest.

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

### -ClusterManifestPathInImageStore
Specifies the relative path in the image store where the cluster manifest should be copied to.

```yaml
Type: String
Parameter Sets: Both, Config
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Code
Specifies that only Service Fabric runtime installation file has to be copied to the image store.

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
Specifies the file path to a Service Fabric runtime installation file. This file can be a MSI or CAB or DEB file.

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

### -CodePackagePathInImageStore
Specifies the relative path in the image store where the Service Fabric runtime installation file should be copied to.

```yaml
Type: String
Parameter Sets: Both, Code
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Specifies that only Service Fabric cluster manifest file has to be copied to the image store.

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

### -ImageStoreConnectionString
Specifies the connection string for the Service Fabric image store. Read more about [the image store connection string](https://docs.microsoft.com/azure/service-fabric/service-fabric-image-store-connection-string).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeoutSec
Specifies the timeout in seconds, for the operation.
By default, the maximum timeout value is limited to 1800 seconds.

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
This cmdlet returns a message that includes the status of the operation.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Register-ServiceFabricClusterPackage](./Register-ServiceFabricClusterPackage.md)

[Remove-ServiceFabricClusterPackage](./Remove-ServiceFabricClusterPackage.md)

[Unregister-ServiceFabricClusterPackage](./Unregister-ServiceFabricClusterPackage.md)
