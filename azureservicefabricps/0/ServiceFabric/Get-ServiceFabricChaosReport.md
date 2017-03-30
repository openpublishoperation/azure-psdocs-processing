---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: D4F9D188-FFB3-4D93-870C-6C6076CBA6AE
online version:
schema: 2.0.0
updated_at: 03/23/2017 20:03 PM
ms.date: 03/23/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricChaosReport.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricChaosReport.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/fac2031a80184883cdb99fa4a8c6e1971ab6aaf2
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricChaosReport

## SYNOPSIS
Gets a report of Chaos results.

## SYNTAX

```
Get-ServiceFabricChaosReport [-StartTimeUtc <DateTime>] [-EndTimeUtc <DateTime>] [-ContinuationToken <String>]
 [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricChaosReport** cmdlet gets a report of a Chaos run which includes the current status and history of [Chaos events](https://docs.microsoft.com/en-us/dotnet/api/system.fabric.chaos.datastructures.chaosevent). You can specify a time range and only Chaos events within this range will be reported. If Chaos was never started, the result will report that.

If there are a large number of Chaos events, the data is reported in batches. Each batch contains a maximum of 100 events. In such a case, a continuation token is returned as part of [ChaosReport](https://docs.microsoft.com/en-us/dotnet/api/system.fabric.chaos.datastructures.chaosreport) object. To get data from subsequent batches, this continuation token will need to be supplied.

For more information about Chaos, see the article [Inducing Chaos](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-controlled-chaos).


## EXAMPLES

### Example 1: View Chaos report
```
PS C:\>$Now = Get-Date
$EndTime = $Now.ToUniversalTime()
$StartTime = $EndTime.AddMinutes(-2)
Get-ServiceFabricChaosReport -StartTimeUtc $StartTime -EndTimeUtc $EndTime -Verbose
```
This command returns the Chaos events from the previous two minutes.

## PARAMETERS

### -ContinuationToken
Specifies a continuation token that this cmdlet passes for the next [Get-ServiceFabricChaosReport](./Get-ServiceFabricChaosReport.md) call. If there are large number of Chaos events, the data is reported in batches. Each batch contains a maximum of 100 events. In such a case, a continuation token is returned as part of **ChaosReport** object. To get data from subsequent batches, this continuation token will need to be supplied.


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTimeUtc
Specifies the end of the time range in Coordinated Universal Time (UTC).

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTimeUtc
Specifies the start of the time range in UTC.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeoutSec
Specifies the timeout period, in seconds for the operation.

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

###  
This cmdlet returns a **ChaosReport** object that represents the report for the Chaos runs.

## NOTES

## RELATED LINKS

[Start-ServiceFabricChaos](./Start-ServiceFabricChaos.md)

[Stop-ServiceFabricChaos](./Stop-ServiceFabricChaos.md)
