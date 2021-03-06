---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: EFDF88E2-DBFD-4868-AB66-E4F5379C55A9
online version:
schema: 2.0.0
updated_at: 03/07/2017 00:03 AM
ms.date: 03/07/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricApplicationPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/bcbc202904350fd056f72db4725d09ae3fc3352c
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Remove-ServiceFabricApplicationPackage

## SYNOPSIS
Removes a Service Fabric application package from the image store.

## SYNTAX

```
Remove-ServiceFabricApplicationPackage [-ApplicationPackagePathInImageStore] <String>
 [-ImageStoreConnectionString] <String> [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-ServiceFabricApplicationPackage** cmdlet removes a Service Fabric application package from the image store.
Run this cmdlet after you register the application package by using the [Register-ServiceFabricApplicationPackage](./Register-ServiceFabricApplicationType.md) cmdlet.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Remove an application package
```
PS C:\>Remove-ServiceFabricApplicationPackage -ImageStoreConnectionString "xstore:DefaultEndpointsProtocol=https;AccountName=[StorageAccountName];AccountKey=[StorageAccountKey];Container=[ContainerName]" -ApplicationPackagePathInImageStore "PersistentToDoListService_v2"
```

This command removes the application package that has the specified image store path.
The cmdlet does prompt you for confirmation before it removes the application package unless you use the parameter "-Confirm".

## PARAMETERS

### -ApplicationPackagePathInImageStore
Specifies the relative path in the image store.
The cmdlet removes the package from the path that this parameter specifies.

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

### -ImageStoreConnectionString
Specifies the connection string for the Service Fabric image store.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not executed.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[Register-ServiceFabricApplicationPackage](./Register-ServiceFabricApplicationType.md)

[Test-ServiceFabricApplicationPackage](./Test-ServiceFabricApplicationPackage.md)

[Deploy and remove applications using PowerShell](https://azure.microsoft.com/documentation/articles/service-fabric-deploy-remove-applications/)
