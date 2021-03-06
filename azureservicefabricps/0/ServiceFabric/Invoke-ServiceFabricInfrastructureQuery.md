---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: E09D6FED-175D-4511-9E66-717A6EB7F495
online version:
schema: 2.0.0
updated_at: 03/06/2017 18:03 PM
ms.date: 03/06/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Invoke-ServiceFabricInfrastructureQuery.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Invoke-ServiceFabricInfrastructureQuery.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/ffcf8444837861c6001f2d5cae123000f4dd6044
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Invoke-ServiceFabricInfrastructureQuery

## SYNOPSIS
Invokes a read-only query on an infrastructure service.

## SYNTAX

```
Invoke-ServiceFabricInfrastructureQuery [-Command] <String> [[-ServiceName] <Uri>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-ServiceFabricInfrastructureQuery** cmdlet invokes a read-only query on an infrastructure service.
The infrastructure service accepts infrastructure-specific commands to allow you to interact directly with the underlying infrastructure by means of the Service Fabric API.
To run this cmdlet, at least one instance of the infrastructure service must be enabled in the cluster configuration.
Currently, this cmdlet is supported only on specially-configured Azure Cloud Services.

This cmdlet supports the Service Fabric platform.
Do not run this cmdlet directly.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

## PARAMETERS

### -Command
Specifies the infrastructure-specific command string to send to the infrastructure service.
The format of supported commands depends on the infrastructure on which the cluster runs.

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

### -ServiceName
Specifies the Uniform Resource Indentifier (URI) of a Service Fabric infrastructure service.
This cmdlet sends the command to the service that this parameter specifies.
The default value is fabric:/System/InfrastructureService.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

###  
This cmdlet accepts an object that contains a **ServiceName** property that identifies the infrastructure service instance to which to send a command.

## OUTPUTS

###  
This cmdlet returns a value that depends on the value of the *Command* parameter, and is determined by the infrastructure.

## NOTES

## RELATED LINKS

[Invoke-ServiceFabricInfrastructureCommand](./Invoke-ServiceFabricInfrastructureCommand.md)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)
