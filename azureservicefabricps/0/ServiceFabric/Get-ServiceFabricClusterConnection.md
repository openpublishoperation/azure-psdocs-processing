---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: AC68A4AD-F230-4E30-83F9-94B88A8A2A32
online version:
schema: 2.0.0
updated_at: 03/06/2017 21:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricClusterConnection.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricClusterConnection.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/34c133f14c1a2a20c26c42fba0c57e54f4de5163
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricClusterConnection

## SYNOPSIS
Gets the current Service Fabric cluster connection.

## SYNTAX

```
Get-ServiceFabricClusterConnection [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricClusterConnection** cmdlet gets the current Service Fabric cluster connection.
To create a cluster connection, use the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get the current cluster connection
```
PS C:\>Get-ServiceFabricClusterConnection
```

This command gets the current Service Fabric cluster connection.

## PARAMETERS

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
This cmdlet returns a **System.Fabric.PowerShell.ClusterConnection** that represents the Service Fabric cluster connection information.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Test-ServiceFabricClusterConnection](./Test-ServiceFabricClusterConnection.md)
