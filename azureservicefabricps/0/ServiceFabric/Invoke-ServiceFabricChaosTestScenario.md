---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 9F010748-70B9-4E00-94C7-EBD0B2983C35
online version:
schema: 2.0.0
updated_at: 03/23/2017 20:03 PM
ms.date: 03/23/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Invoke-ServiceFabricChaosTestScenario.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Invoke-ServiceFabricChaosTestScenario.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/fac2031a80184883cdb99fa4a8c6e1971ab6aaf2
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Invoke-ServiceFabricChaosTestScenario

## SYNOPSIS

This cmdlet is **Obsolete**. Please use [Start-ServiceFabricChaos](./Start-ServiceFabricChaos.md).

Invokes a test scenario to induce iterative failover and faults in a cluster.

## SYNTAX

```
Invoke-ServiceFabricChaosTestScenario [-TimeToRunMinute] <UInt32> [-MaxClusterStabilizationTimeoutSec] <UInt32>
 [-WaitTimeBetweenIterationsSec <UInt32>] [-WaitTimeBetweenFaultsSec <UInt32>] [-MaxConcurrentFaults <UInt32>]
 [-EnableMoveReplicaFaults] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet is **Obsolete**. Please use [Start-ServiceFabricChaos](./Start-ServiceFabricChaos.md).

## PARAMETERS

### -EnableMoveReplicaFaults
Indicates that this cmdlet enables move replica faults.

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

### -MaxClusterStabilizationTimeoutSec
Specifies the maximum time-out period, in seconds, for a cluster to stabilize after a fault before failing the test.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxConcurrentFaults
Specifies the maximum number of concurrent faults.

```yaml
Type: UInt32
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

### -TimeToRunMinute
Specifies the total time, in minutes, for the scenario to run.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitTimeBetweenFaultsSec
Specifies the maximum wait time, in seconds, between consecutive faults.
The larger the value the lower the concurrency.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitTimeBetweenIterationsSec
Specifies the wait time, in seconds, for the duration between iterations.

```yaml
Type: UInt32
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

### UInt32
Represents the time to run.

### UInt32
Represents the maximum stabilization time, in seconds, for the cluster.

## OUTPUTS

### System.Object
This cmdlet returns a **String** object that represents the final status of the test.

## NOTES

## RELATED LINKS

[Start-ServiceFabricChaos](./Start-ServiceFabricChaos.md)
