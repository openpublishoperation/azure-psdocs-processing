---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 97D767C4-EAD7-4D19-A085-2BD1F992C099
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Stop-ServiceFabricTestCommand.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Stop-ServiceFabricTestCommand.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Stop-ServiceFabricTestCommand

## SYNOPSIS
Cancels a running Service Fabric fault operation.

## SYNTAX

```
Stop-ServiceFabricTestCommand -OperationId <Guid> [-ForceCancel] [-Force] [-TimeoutSec <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Stop-ServiceFabricTestCommand** cmdlet cancels the specified fault operation.
Specify the ID of the operation that you provided when you started the fault. The type of faults that can cancelled include Partition Data Loss ([Start-ServiceFabricPartitionDataLoss](./Start-ServiceFabricPartitionDataLoss.md)), Partition Quorum Loss ([Start-ServiceFabricPartitionQuorumLoss](./Start-ServiceFabricPartitionQuorumLoss.md)), Partition Restart ([Start-ServiceFabricPartitionRestart](./Start-ServiceFabricPartitionRestart.md)) and Node State Transition ([Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md)) 

Under normal conditions i.e. without the *Force* parameter, this cmdlet first cancels the fault and attempts to clean up state information. As part of this the fault operation moves into a RollingBack state during the cleanup.
Once the cleanup of the fault completes the final state of the command is Cancelled.

>
>Important Note: If *Force* is true, inconsistent state may be left behind so please use this option with caution. Using the *Force* flag will move the operation to the Cancelled state skipping cleanup. Only to be used if recommended in case of fault operation getting stuck. 
>[Remove-ServiceFabricTestState](./Remove-ServiceFabricTestState.md) should be invoked to remove state that may have been left behind.

## EXAMPLES

### Example 1: Cancel an operation
```
PS C:\>Stop-ServiceFabricTestCommand -OperationId a268cc73-2e30-462b-b3df-3a0d30e5b330
```

This command cancels an operation that has the *OperationId* a268cc73-2e30-462b-b3df-3a0d30e5b330.

## PARAMETERS

### -Force
Indicates that this cmdlet skips the warning message popup and forces the operation to run. 

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

### -ForceCancel
This flag forces the command to be cancelled.
The use of this parameter may leave state information behind. You can specify *Force* only if the fault operation is already in a state of RollingBack else it will be rejected.
The fault operation can be in a RollingBack state only if you previously ran the Stop-ServiceFabricTestCommand without *Force* specified, or if the fault operation rolls back due to a fatal error.

The final state of the command is ForceCancelled.

We do not recommend specifying *Force* unless the command is not proceeding.

>
>Important Note: TestCommandProgressState.RollingBack indicates the system is cleaning up the internal system state caused by executing the command.
>The roll back process does not restore data if the fault operation was a call to [Start-ServiceFabricPartitionDataLoss](./Start-ServiceFabricPartitionDataLoss.md). The system will only clean up its internal state from running the command and
>it will not restore the target partition's data if the command progressed far enough to cause data loss.
>

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

### -OperationId
Specifies a unique identifier for the command that this cmdlet cancels.
You assign this value when you initiated the command.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-ServiceFabricTestCommandStatusList](./Get-ServiceFabricTestCommandStatusList.md)

[Remove-ServiceFabricTestState](./Remove-ServiceFabricTestState.md)

[Start-ServiceFabricPartitionDataLoss](./Start-ServiceFabricPartitionDataLoss.md)
