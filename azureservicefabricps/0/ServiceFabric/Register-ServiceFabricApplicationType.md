---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 9145CA7E-1FF1-44C0-BB40-452161DCB15A
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Register-ServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Register-ServiceFabricApplicationType.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Register-ServiceFabricApplicationType

## SYNOPSIS
Registers a Service Fabric application type.

## SYNTAX

```
Register-ServiceFabricApplicationType [-ApplicationPathInImageStore] <String> [-Async] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Register-ServiceFabricApplicationType** cmdlet registers a Service Fabric application type. The application package must exist in the image store, which can be done with [Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md).

After you register an application type, you can use the [New-ServiceFabricApplication](./New-ServiceFabricApplication.md) cmdlet to create an application instance. Use the [Start-ServiceFabricApplicationUpgrade](./Start-ServiceFabricApplicationUpgrade.md) cmdlet to upgrade an existing application.

When the application type with the specified version is not needed anymore, you can unregister it using [Unregister-ServiceFabricApplicationType](./Unregister-ServiceFabricApplicationType.md) cmdlet.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Register an application type
```
PS C:\>Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "c:\work\PersistentToDoListService" -ImageStoreConnectionString "file:C:\SfDevCluster\Data\ImageStoreShare" -ApplicationPackagePathInImageStore "PersistentToDoListService"
PS C:\>Register-ServiceFabricApplicationType -ApplicationPathInImageStore "PersistentToDoListService"
```

[Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md) copies the application package found in the "c:\work\PersistentToDoListService" folder to the image store. The package is copied at the relative path "PersistentToDoListService" in image store.

[Register-ServiceFabricApplicationType](./Register-ServiceFabricApplicationType.md) command registers the application type found in the relative path "PersistentToDoListService".

### Example 2: Register an application type async
```
PS C:\>Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "c:\work\PersistentToDoListService" -ImageStoreConnectionString "fabric:ImageStore" -ApplicationPackagePathInImageStore "PersistentToDoListService" -CompressPackage
PS C:\>Register-ServiceFabricApplicationType -ApplicationPathInImageStore "PersistentToDoListService" -Async
PS C:\>Get-ServiceFabricApplicationType
```

[Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md) copies the application package found in the "c:\work\PersistentToDoListService" folder to the image store. The application package is copied at the relative path "PersistentToDoListService" in image store. The cmdlet uses compression to reduce the package size.

[Register-ServiceFabricApplicationType](.\Register-ServiceFabricApplicationType.md) command registers the application type found in the relative path "PersistentToDoListService". Register is done async, and it returns as soon as the command is accepted by the cluster.

[Get-ServiceFabricApplicationType](.\Get-ServiceFabricApplicationType.md) gets the application types registered in the cluster. Each application type includes the registration status. The cmdlet can be used to determine when the registration completes.

### Example 3: Register an application type for a large application package
```
PS C:\>Copy-ServiceFabricApplicationPackage -ApplicationPackagePath "c:\work\PersistentToDoListService" -ImageStoreConnectionString "fabric:ImageStore" -ApplicationPackagePathInImageStore "PersistentToDoListService" -CompressPackage -TimeoutSec 2700
PS C:\>Register-ServiceFabricApplicationType -ApplicationPathInImageStore "PersistentToDoListService" -TimeoutSec 2700
```

[Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md) copies the application package found in the "c:\work\PersistentToDoListService" folder to the image store, at the "PersistentToDoListService" image store relative location. Since the initial package is very large, the command compress it and includes a higher timeout to allow enough time for copy.

[Register-ServiceFabricApplicationType](.\Register-ServiceFabricApplicationType.md) command registers the application type found in the relative path "PersistentToDoListService". The command includes a higher timeout to allow work to finish even if the application package is large.

## PARAMETERS

### -ApplicationPathInImageStore
Specifies the relative path of the application type package in the image store. This path was specified by the [Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md) cmdlet when the application package was copied to the image store.

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

### -Async
The command returns as soon as the registration request has been accepted by the cluster. The [Get-ServiceFabricApplicationType](./Get-ServiceFabricApplicationType.md) command can be used to query the status of the registration request. Using this switch avoids having to provide large -TimeoutSec values when registering large application packages.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
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

[Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricApplicationType](./Get-ServiceFabricApplicationType.md)

[Unregister-ServiceFabricApplicationType](./Unregister-ServiceFabricApplicationType.md)

[New-ServiceFabricApplication](./New-ServiceFabricApplication.md)

[Start-ServiceFabricApplicationUpgrade](./Start-ServiceFabricApplicationUpgrade.md)
