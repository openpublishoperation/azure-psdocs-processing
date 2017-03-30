---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: A7669F75-A5B3-4574-8444-CD15A04DF0EE
online version:
schema: 2.0.0
updated_at: 03/06/2017 23:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceDescription.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceDescription.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/50a9c0fba147d91dd2b89665e86e957df994ea7b
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricServiceDescription

## SYNOPSIS
Gets the Service Fabric service description of a service that is running.

## SYNTAX

```
Get-ServiceFabricServiceDescription [-ServiceName] <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricServiceDescription** cmdlet gets the Service Fabric service description of a service that is running.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Get a service description
```
PS C:\>Get-ServiceFabricServiceDescription -ServiceName fabric:/CalcApp/CalcService
```

This command gets the service description for service with the name `fabric:/CalcApp/CalcService`.

## PARAMETERS

### -ServiceName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric service.
This cmdlet gets the service description for the service that you specify.

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
This cmdlet accepts a URI that represents the name of a Service Fabric service.

## OUTPUTS

### System.Object
This cmdlet returns a **[System.Fabric.Description.ServiceDescription](https://docs.microsoft.com/dotnet/api/System.Fabric.Description.ServiceDescription)** object representing the service description for the given service.

## NOTES

## RELATED LINKS

[Get-ServiceFabricService](./Get-ServiceFabricService.md)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
