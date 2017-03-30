---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 578CAE79-F1FF-470E-91B7-814D9DF0917B
online version:
schema: 2.0.0
updated_at: 03/07/2017 19:03 PM
ms.date: 03/07/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricApplication.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/51a9a9cd71a567b6fbd78304cd355499fde42f98
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Remove-ServiceFabricApplication

## SYNOPSIS
Removes a Service Fabric application.

## SYNTAX

```
Remove-ServiceFabricApplication [-ApplicationName] <Uri> [-Force] [-ForceRemove] [-TimeoutSec <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-ServiceFabricApplication** cmdlet removes an application from Service Fabric.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Remove an application
```
PS C:\>Remove-ServiceFabricApplication -ApplicationName fabric:/myapp/persistenttodolist -Force
```

This command removes the application that has the specified URI.
Because this command includes the *Force* parameter, the cmdlet does not prompt you for confirmation before it removes the application.

## PARAMETERS

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application. To get the names (URI) of the currently deployed applications, use [Get-ServiceFabricApplication](./Get-ServiceFabricApplication.md).
The cmdlet removes the application that has the URI that you specify.

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

### -ForceRemove
Indicates that this cmdlet forces removal of the application. This should be used only if removal of the application is timing out.
It is effectively the same as passing -ForceRemove to each internal remove service call. 
Refer to -ForceRemove [Remove-ServiceFabricService](./Remove-ServiceFabricService.md) cmdlet for more details about force removing the services.

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

### -TimeoutSec
Specifies the time-out period, in seconds, for the operation. If the operation times out, the state of the application is undetermined.
Use [Get-ServiceFabricApplicationHealth](./Get-ServiceFabricApplicationHealth.md) to determine the application state or use the -ForceRemove option to forcefully remove the application.

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
The cmdlet is not run and no permanent changes will be made.

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
This cmdlet accepts a URI that represents the name of a Service Fabric application.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricApplication](./Get-ServiceFabricApplication.md)

[New-ServiceFabricApplication](./New-ServiceFabricApplication.md)
