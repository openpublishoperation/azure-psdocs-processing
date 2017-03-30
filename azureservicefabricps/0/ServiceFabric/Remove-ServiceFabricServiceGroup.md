---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 85755368-FB2A-4164-B826-74E5A5A52328
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricServiceGroup.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricServiceGroup.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Remove-ServiceFabricServiceGroup

## SYNOPSIS
Removes a Service Fabric service group.

## SYNTAX

```
Remove-ServiceFabricServiceGroup [-ServiceName] <Uri> [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-ServiceFabricServiceGroup** cmdlet removes a Service Fabric service group.
A service must be running before you can remove it.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet and then the [Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md) cmdlet.

## EXAMPLES

### Example 1: Remove a service group
```
PS C:\>Remove-ServiceFabricServiceGroup -ServiceName fabric:/myapp/persistenttodolist/svc1 -Force
```

This command removes the Service Fabric service group named fabric:/myapp/persistenttodolist/svc1.
Because the command specifies the *Force* parameter, the cmdlet does not prompt you for confirmation.

## PARAMETERS

### -Force
Forces the command to run without asking for user confirmation.

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

### -ServiceName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric service group.

```yaml
Type: Uri
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

### System.Uri
This cmdlet accepts a URI that represents the name of a Service Fabric service group.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[New-ServiceFabricServiceGroup](./New-ServiceFabricServiceGroup.md)

[Update-ServiceFabricServiceGroup](./Update-ServiceFabricServiceGroup.md)
