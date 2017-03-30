---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 25F1C2E1-5AB4-42AF-AD53-4AAA1EBE8B4B
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Resume-ServiceFabricClusterUpgrade.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Resume-ServiceFabricClusterUpgrade.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Resume-ServiceFabricClusterUpgrade

## SYNOPSIS
Resumes an unmonitored Service Fabric cluster upgrade.

## SYNTAX

```
Resume-ServiceFabricClusterUpgrade [-UpgradeDomainName] <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Resume-ServiceFabricClusterUpgrade** cmdlet resumes an unmonitored manual Service Fabric cluster upgrade.
Service Fabric upgrades one upgrade domain at a time.
For unmonitored manual upgrades, after Service Fabric finishes an upgrade domain, it waits for you to run this cmdlet to proceed to the next upgrade domain.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet and then the [Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md) cmdlet.

## EXAMPLES

### Example 1: Resume an upgrade
```
PS C:\>Resume-ServiceFabricClusterUpgrade -UpgradeDomainName "MYUD02"
```

This command resumes the upgrade process after it finishes an upgrade domain.
The command specifies MYUD02 as the next upgrade domain.

## PARAMETERS

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

### -UpgradeDomainName
Specifies the name of the next upgrade domain to upgrade.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricClusterUpgrade](./Get-ServiceFabricClusterUpgrade.md)

[Start-ServiceFabricClusterUpgrade](./Start-ServiceFabricClusterUpgrade.md)
