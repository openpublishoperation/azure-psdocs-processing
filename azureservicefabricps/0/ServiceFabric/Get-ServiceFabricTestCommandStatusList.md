---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 26459CBC-9296-4B65-A298-E6B31EF65865
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricTestCommandStatusList.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricTestCommandStatusList.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricTestCommandStatusList

## SYNOPSIS
Gets the list of all the fault operations triggered in the cluster and their status

## SYNTAX

```
Get-ServiceFabricTestCommandStatusList [-StateFilter <TestCommandStateFilter>]
 [-TypeFilter <TestCommandTypeFilter>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricTestCommandStatusList** gets the list of the fault operations triggered in the cluster and their status. The list of faults tracked by this operation include Partition Data Loss ([Start-ServiceFabricPartitionDataLoss](./Start-ServiceFabricPartitionDataLoss.md)), Partition Quorum Loss ([Start-ServiceFabricPartitionQuorumLoss](./Start-ServiceFabricPartitionQuorumLoss.md)), Partition Restart ([Start-ServiceFabricPartitionRestart](./Start-ServiceFabricPartitionRestart.md)) and Node State Transition ([Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md)).

The Operation ID returned can be used to get additional details about the fault operation using the get progress APIs for the respective fault and/or to cancel the fault using the [Stop-ServiceFabricTestCommand](./Stop-ServiceFabricTestCommand.md) command. The mapping from TestCommandType to the progress API can be found below

| TestCommandType | Get Progess Command |
| --- | --- |
| PartitionDataLoss | [Get-ServiceFabricPartitionDataLossProgress](./Get-ServiceFabricPartitionDataLossProgress) |
| PartitionQuorumLoss | [Get-ServiceFabricPartitionQuorumLossProgress](./Get-ServiceFabricPartitionQuorumLossProgress) |
| PartitionRestart | [Get-ServiceFabricPartitionRestartProgress](./Get-ServiceFabricPartitionRestartProgress) |
| NodeTransition | [Get-ServiceFabricNodeTransitionProgress](./Get-ServiceFabricNodeTransitionProgress) |
## EXAMPLES

### Example 1: Get status of cancelled test commands
```
PS C:\>Get-ServiceFabricTestCommandStatusList -StateFilter Cancelled
OperationId                              State     TestCommandType
-----------                              -----     ---------------
a268cc73-2e30-462b-b3df-3a0d30e5b330 Cancelled PartitionQuorumLoss
```

This command gets the status of fault operations that have been cancelled.
In this example, the result has one fault operation.

### Example 2: Get status of all test commands
```
PS C:\>Get-ServiceFabricTestCommandStatusList
OperationId                              State     TestCommandType
-----------                              -----     ---------------
aeaceca9-320d-4f7b-84e8-3cc13c29a974 Completed PartitionQuorumLoss
0e3fa169-dec0-46d1-8eff-2f1a4a3f5fde Completed    PartitionRestart
a268cc73-2e30-462b-b3df-3a0d30e5b330 Cancelled PartitionQuorumLoss
51ed168c-bb22-47d5-97f9-6b74b353bb33 Completed PartitionQuorumLoss
ebd322c2-b1d3-46a7-b254-3cc42e6ca2d1 Completed    PartitionRestart
d3f12b09-6a90-4745-a4fc-3f92149a7419 Completed   PartitionDataLoss
```

This command gets the status of all fault operations.
The returned list contains five completed operations, and one cancelled operation.

## PARAMETERS

### -StateFilter
This parameter can be used to filter the list of operations returned based on the current Status of the fault operation. You can use this to limit the results returned to the ones that interest you. 

```yaml
Type: TestCommandStateFilter
Parameter Sets: (All)
Aliases: 
Accepted values: Default, Running, RollingBack, CompletedSuccessfully, Failed, Cancelled, ForceCancelled, All

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

### -TypeFilter
This parameter can be used to filter the list of operations returned based on the type of the fault operation. You can use this to limit the results returned to the fault types that interest you. 

```yaml
Type: TestCommandTypeFilter
Parameter Sets: (All)
Aliases: 
Accepted values: Default, PartitionDataLoss, PartitionQuorumLoss, PartitionRestart, All

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

[Stop-ServiceFabricTestCommand](./Stop-ServiceFabricTestCommand.md)

[Get-ServiceFabricPartitionDataLossProgress](./Get-ServiceFabricPartitionDataLossProgress)

[Get-ServiceFabricPartitionQuorumLossProgress](./Get-ServiceFabricPartitionQuorumLossProgress)

[Get-ServiceFabricPartitionRestartProgress](./Get-ServiceFabricPartitionRestartProgress)

[Get-ServiceFabricNodeTransitionProgress](./Get-ServiceFabricNodeTransitionProgress)
