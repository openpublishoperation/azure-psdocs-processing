---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 701917EF-185C-433D-A0B2-A63DEE0E96C3
online version:
schema: 2.0.0
updated_at: 03/28/2017 20:03 PM
ms.date: 03/28/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricClusterConnection.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricClusterConnection.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/16a577fb6a51f5ca50120cc3307348c9086eb9f5
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Test-ServiceFabricClusterConnection

## SYNOPSIS
Checks and confirms (by returning "True") that you are connected to a Service Fabric cluster.

## SYNTAX

```
Test-ServiceFabricClusterConnection [-AllowNetworkConnectionOnly] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Test-ServiceFabricClusterConnection** cmdlet tests whether a connection to a Service Fabric cluster exists. Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Test that a current connection to a cluster exists
```
PS C:\>Test-ServiceFabricClusterConnection
True
```
This command verifies that a current connection to a Service Fabric cluster exists.

### Example 2: Test that a current connection to a cluster exists
```
PS C:\>Test-ServiceFabricClusterConnection
```
Test-ServiceFabricClusterConnection : Cluster connection instance is null

In this case, a current connection to a Service Fabric cluster does not exist and has to be set up using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## PARAMETERS

### -AllowNetworkConnectionOnly
When set, the cmdlet will return "True" if it can connect to the cluster even when system services are unresponsive. That is, as long as an underlying network connection can be established to the cluster, it will return "True".

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
This cmdlet supports the following common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns $True if the Service Fabric cluster connection is valid, or, if it is not valid, this cmdlet returns $False.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
