---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 4BC03E59-F564-4678-A6DE-83974795422C
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Stop-ServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Stop-ServiceFabricNode.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Stop-ServiceFabricNode

## SYNOPSIS
**OBSOLETE**. Please use the [Start-ServiceFabricNodeTransition](./Start-ServiceFabricNodeTransition.md) cmdlet instead.

## SYNTAX

```
Stop-ServiceFabricNode [-NodeName] <String> [[-NodeInstanceId] <BigInteger>]
 [-CommandCompletionMode <CompletionMode>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
**OBSOLETE**. The **Stop-ServiceFabricNode** cmdlet stops a node in a Service Fabric cluster.

## PARAMETERS

### -CommandCompletionMode
Specifies whether the action waits for the restart to complete.

```yaml
Type: CompletionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeInstanceId
Specifies a node instance ID.

```yaml
Type: BigInteger
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
Specifies the name of a Service Fabric node to stop.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
Specifies the name of a Service Fabric node.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Testability.StopNode** object that represents the operation result.

## NOTES

## RELATED LINKS

[Disable-ServiceFabricNode](./Disable-ServiceFabricNode.md)

[Enable-ServiceFabricNode](./Enable-ServiceFabricNode.md)

[Get-ServiceFabricNode](./Get-ServiceFabricNode.md)

[Restart-ServiceFabricNode](./Restart-ServiceFabricNode.md)

[Start-ServiceFabricNode](./Start-ServiceFabricNode.md)
