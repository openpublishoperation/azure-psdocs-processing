---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 51657577-F2A0-4D22-822C-3586F0A70B04
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Copy-ServiceFabricApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Copy-ServiceFabricApplicationPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Copy-ServiceFabricApplicationPackage

## SYNOPSIS
Copies a Service Fabric application package to the image store.

## SYNTAX

### SkipCopy
```
Copy-ServiceFabricApplicationPackage [-ApplicationPackagePath] <String>
 [[-ImageStoreConnectionString] <String>] [[-ApplicationPackagePathInImageStore] <String>] [-ShowProgress]
 [-ShowProgressIntervalMilliseconds <Int32>] [-CompressPackage] [-UncompressPackage] [-SkipCopy]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

### Copy
```
Copy-ServiceFabricApplicationPackage [-ApplicationPackagePath] <String> [-ImageStoreConnectionString] <String>
 [[-ApplicationPackagePathInImageStore] <String>] [-ShowProgress] [-ShowProgressIntervalMilliseconds <Int32>]
 [-CompressPackage] [-UncompressPackage] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Copy-ServiceFabricApplicationPackage** cmdlet copies a Service Fabric application package to the image store. This cmdlet can also be used for compressing and uncompressing a Service Fabric application package without actually copying it to the image store.

After copying the application package, use the [Register-ServiceFabricApplicationType](.\Register-ServiceFabricApplicationType.md) cmdlet to register the application type.

After registering the application package, use the [Remove-ServiceFabricApplicationPackage](.\Remove-ServiceFabricApplicationPackage.md) cmdlet to remove the application package.

To manage Service Fabric clusters, start Windows PowerShell by using the **Run as administrator** option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](.\Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Copy an application package
```
PS C:\> Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\ApplicationPackages\PersistentToDoListService" -ImageStoreConnectionString "fabric:ImageStore"
```

This command copies the application package to the cluster's image store. When **ApplicationPackagePathInImageStore** parameter is not specified, it is defaulted to the folder name. In this example, **ApplicationPackagePathInImageStore** will default to PersistentToDoListService

### Example 2: Copy an application package to a specific directory in the image store
```
PS C:\> Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\ApplicationPackages\PersistentToDoListService" -ImageStoreConnectionString "fabric:ImageStore" -ApplicationPackagePathInImageStore "PersistentToDoListService_v2"
```

This command copies the application package to PersistentToDoListService_v2 directory in the cluster's image store.

### Example 3: Copy a compressed application package to a specific directory in the image store
```
PS C:\> Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\ApplicationPackages\PersistentToDoListService" -ImageStoreConnectionString "fabric:ImageStore" -ApplicationPackagePathInImageStore "PersistentToDoListService_v2" -CompressPackage
```

This command compresses all sub-directories under the service directory and then copies the application package to PersistentToDoListService_v2 directory in the cluster's image store.

### Example 4: Show progress bar for the copy operation on PowerShell window
```
PS C:\> Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\ApplicationPackages\PersistentToDoListService" -ImageStoreConnectionString "fabric:ImageStore" -ApplicationPackagePathInImageStore "PersistentToDoListService_v2" -ShowProgress -ShowProgressIntervalMilliseconds 500
```

This command shows a progress bar on the PowerShell window while copying the application package to PersistentToDoListService_v2 directory in the cluster's image store. The progress bar is refreshing every 500ms.

### Example 5: Compress the application package on the local machine without copying to image store
```
PS C:\> Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\ApplicationPackages\PersistentToDoListService" -CompressPackage -SkipCopy
```

This command compresses all sub-directories under the service directory without actually copying the application package to the cluster's image store.

### Example 6: Uncompress the application package on the local machine without copying to image store
```
PS C:\> Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\ApplicationPackages\PersistentToDoListService" -UncompressPackage -SkipCopy
```

This command uncompresses all sub-directories under the service directory without actually copying the application package to the cluster's image store.

## PARAMETERS

### -ApplicationPackagePath
Specifies the relative path of an application package.
The cmdlet copies the package from the path that you specify.

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

### -ApplicationPackagePathInImageStore
Specifies the relative path in the image store where the application package should be copied to.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompressPackage
Specifies to compresses all sub-directories under the service directory (code/config/data packages) in the application package. If **SkipCopy** is not specified, the folders will be compressed before copying the application package to the image store.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageStoreConnectionString
Specifies the connection string for the Service Fabric image store. Read more about [the image store connection string](https://docs.microsoft.com/azure/service-fabric/service-fabric-image-store-connection-string).

```yaml
Type: String
Parameter Sets: SkipCopy
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Copy
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowProgress
Specifies to shows a progress bar in the PowerShell window while copying the application package to the image store.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowProgressIntervalMilliseconds
Specifies the frequency at which the progress bar is refreshed in the PowerShell window while copying the application package to the image store.

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

### -SkipCopy
Specifies to skip copying the application package to image store. This should be used when application package needs to be just compressed or uncompressed without actually copying the application package to the image store.

```yaml
Type: SwitchParameter
Parameter Sets: SkipCopy
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

### -UncompressPackage
Specifies to uncompresses all sub-directories under the service directory (code/config/data packages) in the application package. This can be used with **SkipCopy** to uncompress the application package locally without actually copying the application package to the image store.

```yaml
Type: SwitchParameter
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
This cmdlet returns a message that includes the status of the copy operation.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Register-ServiceFabricApplicationType](./Register-ServiceFabricApplicationType.md)

[Remove-ServiceFabricApplicationPackage](./Remove-ServiceFabricApplicationPackage.md)
