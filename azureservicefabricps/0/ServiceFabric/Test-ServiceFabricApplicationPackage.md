---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 81C3B5F4-6B48-47CB-AC09-3193F3F86E25
online version:
schema: 2.0.0
updated_at: Invalid date
ms.date: Invalid date
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricApplicationPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Test-ServiceFabricApplicationPackage

## SYNOPSIS
Validates a Service Fabric application package.

## SYNTAX

```
Test-ServiceFabricApplicationPackage [-ApplicationPackagePath] <String> [-ApplicationParameter <Hashtable>]
 [-ImageStoreConnectionString <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Test-ServiceFabricApplicationPackage** cmdlet validates a Service Fabric application package to ensure it respects the Service Fabric packaging requirements. Read more about [the Service Fabric application model](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model).

If you specify the image store connection string, the package is also validated against previous versions of the application that are provisioned in the cluster. For example, the cmdlet can detect that an application package with the same version but different content was already provisioned in the image store.

After you validate a package, use the [Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md) cmdlet to copy it to the image store.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Validate an application package locally, without access to the image store
```
PS C:\>Test-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\CalculatorApp" -ApplicationParameter @{ "StatelessServiceInstanceCount"="-1"}
```

This command validates the application package found in the specified path. It includes the application parameters to be verified. 
The cmdlet does not specify the image store connection string because the application is still in the development phase or the cluster connection is not yet known.

### Example 2: Validate an application package, locally and against any previous versions in the image store
```
PS C:\>Test-ServiceFabricApplicationPackage -ApplicationPackagePath "C:\CalculatorApp" -ImageStoreConnectionString "file:C:\SfDevCluster\Data\ImageStoreShare"
```

This command validates the application package found in the specified path. It provides the image store connection string for more validation against application versions already in the image store.


## PARAMETERS

### -ApplicationPackagePath
Specifies the path to an application package. The cmdlet checks that the application package in the path is valid.

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

### -ApplicationParameter
Specifies the overrides for application parameters as a dictionary, such as `@{"key1"="value1"; "key2"="value2"}`. The application parameters must be defined in the application manifest. Otherwise, the validation fails pointing to the potentially misspelled application parameter name.

You need to pass in the application parameters so the cmdlet can perform the same validation as the [New-ServiceFabricApplication](./New-ServiceFabricApplication.md) or [Start-ServiceFabricApplicationUpgrade](./Start-ServiceFabricApplicationUpgrade.md) operations. This is useful as a sanity check to ensure the application package and the application parameters are correct. If the application has parameters that are not specified, validation is skipped.

Read more about [application parameters](https://docs.microsoft.com/azure/service-fabric/service-fabric-manage-multiple-environment-app-configuration).

```yaml
Type: Hashtable
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

If you specify this parameter, the cmdlet performs additional validations against previously deployed versions currently in the store. It is recommended you specify the image store connection string, unless the application is still being developed or the cluster information is not known.

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
This cmdlet returns $True if the Service Fabric application package is valid and $False otherwise.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Copy-ServiceFabricApplicationPackage](./Copy-ServiceFabricApplicationPackage.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Remove-ServiceFabricApplicationPackage](./Remove-ServiceFabricApplicationPackage.md)
