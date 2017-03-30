---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 13C206CD-D1A4-4BAE-8014-4D7AB68D147D
online version:
schema: 2.0.0
updated_at: 03/28/2017 20:03 PM
ms.date: 03/28/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricClusterConfiguration.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricClusterConfiguration.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/16a577fb6a51f5ca50120cc3307348c9086eb9f5
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricClusterConfiguration

## SYNOPSIS
Gets the latest JSON format cluster configuration.

## SYNTAX

```
Get-ServiceFabricClusterConfiguration [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricClusterConfiguration** cmdlet gets the latest cluster configuration in JavaScript Object Notation (JSON) format.

To run this cmdlet, you must first establish a connection by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

Note: At this time this cmdlet only applicable to on-premise Standalone deployments. If executed against a cluster which does not have the UpgradeOrchestrationService Fabric system service, the request will time out. 

## EXAMPLES

### Example 1: Get cluster configuration
```
PS C:\>Connect-ServiceFabricCluster -ConnectionEndpoint "ServiceFabric01.ContosoCloudApp.net:19000"
PS C:\>Get-ServiceFabricClusterConfiguration
```

The first command creates a connection to the specified cluster.

The second command gets the latest cluster configuration in JSON format.

## PARAMETERS

### -TimeoutSec
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

### None
This cmdlet returns the latest cluster configuration in JavaScript Object Notation (JSON) format.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConfigurationUpgradeStatus](./Get-ServiceFabricClusterConfigurationUpgradeStatus.md)

[Start-ServiceFabricClusterConfigurationUpgrade](./Start-ServiceFabricClusterConfigurationUpgrade.md)
