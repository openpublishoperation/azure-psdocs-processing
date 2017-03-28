---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: B9E95A72-E760-4407-8DF1-94BF0E35A28F
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricNodeState.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricNodeState.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Remove-ServiceFabricNodeState

## SYNOPSIS
Notifies Service Fabric that the state on a node has been removed by an external mechanism.

## SYNTAX

```
Remove-ServiceFabricNodeState [-NodeName] <String> [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-ServiceFabricNodeState** cmdlet notifies Service Fabric that for a particular node in a cluster which is down, that any services or state on that node are lost and unrecoverable, and because of that, it has been removed. For instance, this can happen if a hard disk crashes. This command is also useful for downscaling without automatic node removal.

For stateful services, Service Fabric will wait for state and services on a down node to be recovered. In some cases, the administrator knows that a node (and its state) has been permanently lost. In these cases this operation should be called in order to get Service Fabric to stop waiting for that node to recover.
Do not run this cmdlet if the node is expected to come back up with its state intact.

The process to remove a node consists of deactivating the node, removing node configurations, and then, finally, removing the node state. In the case of a crash, the first two steps have already happened.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Inform Service Fabric about node state removal
```
PS C:\>Remove-ServiceFabricNodeState -NodeName "DB.41"
```

This command informs Service Fabric that node state for DB.41 has been removed.

### Example 2: Inform Service Fabric about node state removal with options
```
PS C:\>Remove-ServiceFabricNodeState -NodeName "DB.41" -Confirm
```

This command ensures that a confirmation window specific to this operation pops up when run.

## PARAMETERS

### -Force
Forces the command to run without asking for user confirmation. Do not select "Confirm" if selecting this switch parameter.

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

### -NodeName
Specifies the name of a Service Fabric node.
The cmdlet removes the node state for the node that you specify.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Prompts you for confirmation before running the cmdlet. By default, PowerShell asks for confirmation before running this operation. This switch adds an additional confirmation. Do not select "Force" if selecting this switch parameter.

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
Shows what would happen if the cmdlet runs. The cmdlet is not actually run.
This is a PowerShell standard parameter. Selecting this option does not check for the success or result of this operation.

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

### String
This cmdlet accepts the name of a Service Fabric node.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string. The value is either success or an error message.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
