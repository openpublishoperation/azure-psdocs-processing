---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricNodeTransitionProgress.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricNodeTransitionProgress.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Get-ServiceFabricNodeTransitionProgress

## SYNOPSIS
Gets the progress of a node transition operation.

## SYNTAX

```
Get-ServiceFabricNodeTransitionProgress -OperationId <Guid> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
A node transition operation is an operation to start or stop a Service Fabric node.
The **Get-ServiceFabricNodeTransitionProgress** cmdlet gets the progress of a node transition operation that is started by using the [Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md) cmdlet.
This cmdlet returns an object of type [System.Fabric.NodeTransitionProgress](https://docs.microsoft.com/dotnet/api/system.fabric.nodetransitionprogress).
The **State** property of that object indicates the current state of the operation.
For example, state value **Running** means the operation is in progress.
Completed means it finished successfully.

For more information, see [Replacing the Start Node and Stop node APIs with the Node Transition API](https://docs.microsoft.com/azure/service-fabric/service-fabric-node-transition-apis).

## EXAMPLES

### Example 1: Check progress of an operation
```
PS C:\> $CurrentProgress = Get-ServiceFabricNodeTransitionProgress -OperationId c645433e-a68f-4c8a-8cfb-076d339726a8

PS C:\> $CurrentProgress.State

Running
```

In the example above, the progress an operation is queried and the result indicates that the operation is in the **Running** state.

### Example 2: Troubleshoot failed operation
```
PS C:\> $CurrentProgress = Get-ServiceFabricNodeTransitionProgress -OperationId 6f2bedbe-72c7-4d25-891d-4e070e8809a0

PS C:\> $CurrentProgress.State

Faulted

PS C:\> $CurrentProgress.Result.Exception.ErrorCode

InstanceIdMismatch
```

In the example above, the progress an operation is queried. The result indicates that the operation is in the **Faulted** state and that the **Result.Exception.ErrorCode** value is InstanceIdMismatch. This implies that an incorrect *NodeInstanceId* was provided.
Note that until the operation reaches a terminal state, the **Result** object is $Null.

## PARAMETERS

### -OperationId
Specify the unique ID used to track an operation.
This is the same value that you used to start the operation by using [Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md).

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeoutSec
Specifies the time-out value, in seconds, for this cmdlet.

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

### System.Fabric.NodeTransitionProgress

## NOTES

## RELATED LINKS

[Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md)

[Replacing the Start Node and Stop node APIs with the Node Transition API](https://docs.microsoft.com/azure/service-fabric/service-fabric-node-transition-apis)
