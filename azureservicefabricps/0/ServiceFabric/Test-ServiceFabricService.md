---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 0F403FD1-EA91-4040-BD9E-D289B59F0E01
online version:
schema: 2.0.0
updated_at: 03/13/2017 18:03 PM
ms.date: 03/13/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Test-ServiceFabricService.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/153e6542b0214a79c84e355c2e8dec6fd11c5847
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Test-ServiceFabricService

## SYNOPSIS
Validates the health and availability of a Service Fabric service.

## SYNTAX

```
Test-ServiceFabricService [-ServiceName] <Uri> [-MaxStabilizationTimeoutSec] <Int32> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Test-ServiceFabricService** cmdlet validates the availability and health of the specified Service Fabric service.
This cmdlet verifies that the service is at the target replica set size and that the service is healthy.
This cmdlet also validates that all replicas belonging to the service are ready and not in an transitional state like InBuild ([ServiceReplicaStatus](https://docs.microsoft.com/en-us/dotnet/api/system.fabric.query.servicereplicastatus)).
Use this cmdlet to verify that your service is stable after inducing any fault into the system.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Test a service
```
PS C:\>Test-ServiceFabricService -ServiceName fabric:/SvcName -MaxStabilizationTimeoutSec 240
```

This command tests the specified service to make sure that it is stable within 240 seconds.

## PARAMETERS

### -MaxStabilizationTimeoutSec
Specifies the maximum time-out period, in seconds, for the cluster to stabilize before failing the validate command.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifies the name of the service to validate.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Uri
Represents the name of a Service Fabric service.

## OUTPUTS

### System.Object
This cmdlet returns a **String** object that represents the status of validation.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricService](./Get-ServiceFabricService.md)

[New-ServiceFabricService](./New-ServiceFabricService.md)

[Remove-ServiceFabricService](./Remove-ServiceFabricService.md)

[Test-ServiceFabricService](./Test-ServiceFabricService.md)

[Update-ServiceFabricService](./Update-ServiceFabricService.md)
