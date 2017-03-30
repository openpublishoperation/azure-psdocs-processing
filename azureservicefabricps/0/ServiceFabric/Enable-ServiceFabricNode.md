---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 6DB4FBB9-B046-47D5-922C-12501D1F3403
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Enable-ServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Enable-ServiceFabricNode.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Enable-ServiceFabricNode

## SYNOPSIS
Enables a Service Fabric node.

## SYNTAX

```
Enable-ServiceFabricNode [-NodeName] <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-ServiceFabricNode** cmdlet enables a previously disabled Service Fabric node.
Use this cmdlet after a node has been disabled and the administrative task completed.
This cmdlet can also cancel an existing [Disable-ServiceFabricNode](./Disable-ServiceFabricNode.md) command.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Enable a node
```
PS C:\>Enable-ServiceFabricNode -NodeName "DB.41"
```

This command enables a node named DB.41.

## PARAMETERS

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet enables the node that you specify.

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
This cmdlet returns a message that includes the status of the operation.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Disable-ServiceFabricNode](./Disable-ServiceFabricNode.md)

[Get-ServiceFabricNode](./Get-ServiceFabricNode.md)
