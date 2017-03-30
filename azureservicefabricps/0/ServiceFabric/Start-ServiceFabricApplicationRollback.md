---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 169F0E6F-8E42-41DD-B406-0A232E380A8D
online version:
schema: 2.0.0
updated_at: 03/23/2017 20:03 PM
ms.date: 03/23/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricApplicationRollback.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricApplicationRollback.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/fac2031a80184883cdb99fa4a8c6e1971ab6aaf2
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Start-ServiceFabricApplicationRollback

## SYNOPSIS
Starts rolling back a Service Fabric application upgrade.

## SYNTAX

```
Start-ServiceFabricApplicationRollback [-ApplicationName] <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Start-ServiceFabricApplicationRollback** cmdlet manually starts rolling back a pending upgrade.
If the command finishes successfully, then the cmdlet has registered the intent to roll back the upgrade with Service Fabric.
To monitor the status of the rollback, use the [Get-ServiceFabricApplicationUpgrade](./Get-ServiceFabricApplicationUpgrade.md) cmdlet.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Roll back an existing application upgrade
```
PS C:\>Start-ServiceFabricApplicationRollback -ApplicationName fabric:/MyApp
```

This command starts rolling back any existing application upgrade for fabric:/MyApp.

## PARAMETERS

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application.
The cmdlet rolls back the upgrade for the Service Fabric that this parameter specifies.

```yaml
Type: Uri
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

### None
This cmdlet does not generate any output.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricApplicationUpgrade](./Get-ServiceFabricApplicationUpgrade.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Start-ServiceFabricApplicationUpgrade](./Start-ServiceFabricApplicationUpgrade.md)

[Start-ServiceFabricClusterRollback](./Start-ServiceFabricClusterRollback.md)

[Update-ServiceFabricClusterUpgrade](./Update-ServiceFabricClusterUpgrade)
