---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 1F7B207A-83D7-45F1-AC0C-E3222D98D54D
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricCluster.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Remove-ServiceFabricCluster

## SYNOPSIS
Removes a Service Fabric cluster.

## SYNTAX

```
Remove-ServiceFabricCluster [-ClusterConfigurationFilePath] <String> [-DeleteLog] [-Force]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-ServiceFabricCluster** cmdlet removes a Service Fabric cluster based on a cluster configuration file in JavaScript Object Notation (JSON) format.
The configuration includes target computers from which the cmdlet removes Fabric nodes.

## EXAMPLES

### Example 1: Remove a cluster
```
PS C:\>Remove-ServiceFabricCluster -ClusterConfigurationFilePath "D:\standalone\ClusterConfig.Unsecure.DevCluster.json"
```

Removes the Service Fabric cluster nodes based on computers specified in the cluster configuration file.

## PARAMETERS

### -ClusterConfigurationFilePath
Specifies the path of the cluster configuration JSON file.
The configuration describes target computers from which Fabric nodes are removed.

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

### -DeleteLog
Indicates that the cmdlet removes log files as part of cluster removal.

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

### -Force
{{Fill Force Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[New-ServiceFabricCluster](./New-ServiceFabricCluster.md)
