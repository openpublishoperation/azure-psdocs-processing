---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 298F2C12-F1BE-4341-B5A0-4C45CF45EB52
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Unregister-ServiceFabricClusterPackage.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Unregister-ServiceFabricClusterPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Unregister-ServiceFabricClusterPackage

## SYNOPSIS
Unregisters Service Fabric runtime installation version and/or cluster manifest version from the cluster.

## SYNTAX

### Both (Default)
```
Unregister-ServiceFabricClusterPackage -CodePackageVersion <String> -ClusterManifestVersion <String> [-Force]
 [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Code only
```
Unregister-ServiceFabricClusterPackage [-Code] -CodePackageVersion <String>
 [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Config
```
Unregister-ServiceFabricClusterPackage [-Config] -ClusterManifestVersion <String> 
[-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Unregister-ServiceFabricClusterPackage** cmdlet unregisters Service Fabric runtime installation version and/or cluster manifest version from the cluster. The versions should be unregistered from the cluster if the versions are no longer used. This cmdlet will fail if the version is currently being used by the cluster.

The list of all registered Service Fabric runtime installation versions registered with the cluster can be obtained by using the [Get-ServiceFabricRegisteredClusterCodeVersion](./Get-ServiceFabricRegisteredClusterCodeVersion.md) cmdlet.

The list of all registered cluster manifest versions registered with the cluster can be obtained by using the [Get-ServiceFabricRegisteredClusterConfigVersion](./Get-ServiceFabricRegisteredClusterConfigVersion.md) cmdlet.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Unregister both cluster manifest and runtime installation version from cluster
```
PS C:\>Unregister-ServiceFabricClusterPackage -ClusterManifestVersion "V2" -CodePackageVersion "2.0.59.0"
```

This command unregisters cluster manifest version "V2" and runtime installation version "2.0.59.0" from the cluster.

### Example 1: Unregister just the cluster manifest version from cluster
```
PS C:\>Unregister-ServiceFabricClusterPackage -Config -ClusterManifestVersion "V2"
```

This command unregisters cluster manifest version "V2" from the cluster.

### Example 1: Unregister just the runtime installation version from cluster
```
PS C:\>Unregister-ServiceFabricClusterPackage -Code -CodePackageVersion "2.0.59.0"
```

This command unregisters runtime installation version "2.0.59.0" from the cluster.

## PARAMETERS

### -ClusterManifestVersion
Specifies the cluster manifest version to unregister from the cluster.

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
Indicates that only the Service Fabric runtime installation version needs to be unregistered from the cluster.

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

### -CodePackageVersion
Specifies the runtime installation version to unregister from the cluster.

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
Indicates that only the Service Fabric cluster manifest version needs to be unregistered from the cluster.

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

### -Force
Forces the command to run without asking for user confirmation.

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
The cmdlet is not run.

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

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Copy-ServiceFabricClusterPackage](./Copy-ServiceFabricClusterPackage.md)

[Register-ServiceFabricClusterPackage](./Register-ServiceFabricClusterPackage.md)

[Get-ServiceFabricRegisteredClusterCodeVersion](./Get-ServiceFabricRegisteredClusterCodeVersion.md)

[Get-ServiceFabricRegisteredClusterConfigVersion](./Get-ServiceFabricRegisteredClusterConfigVersion.md)
