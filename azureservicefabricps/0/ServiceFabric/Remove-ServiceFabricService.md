---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: D081C4DD-6311-46E4-9162-C32BDD48FF32
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Remove-ServiceFabricService.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Remove-ServiceFabricService

## SYNOPSIS
Removes an existing Service Fabric service.

## SYNTAX

```
Remove-ServiceFabricService [-ServiceName] <Uri> [-Force] [-ForceRemove] [-TimeoutSec <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-ServiceFabricService** cmdlet removes an existing Service Fabric service.
A service must be running before you can remove it.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Remove a service fabric
```
PS C:\>Remove-ServiceFabricService -ServiceName fabric:/myapp/persistenttodolist/svc1 -Force
```

This command removes the specified Service Fabric service.
Because the command includes the *Force* parameter, the cmdlet does not prompt you for confirmation.

### Example 2: ForceRemove a service fabric service with Confirmation
```
PS C:\>Remove-ServiceFabricService -ServiceName fabric:/myapp/persistenttodolist/svc1 -Confirm -ForceRemove
```

This command force removes the specified Service Fabric service.
Because the command includes the *Confirm* parameter, the cmdlet will prompt you to confirm if it is the intended service name you want to execute the operation on. After the confirmation, the service will be removed ungracefully because of the *ForceRemove* parameter.

### Example 3: ForceRemove a service fabric service with Timeout
```
PS C:\>Remove-ServiceFabricService -ServiceName fabric:/myapp/persistenttodolist/svc1 -TimeoutSec 10 -ForceRemove
```

This command force remove the specified Service Fabric service.
Because the command includes the *Timeout* parameter, the operation will timeout if the operation cannot complete in specified time.

## PARAMETERS

### -Force
Forces the command to run without asking for user confirmation. Powershell won't ask for the user confirmation to execute the command.

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
Indicates that this command forces removal of the Service Fabric service. This should be used only if the removal of the service is timing out.
For example: IF Remove-ServiceFabricService is timing out and the replicas of the service are still present then, this means that the service is stuck in ChangeRole/Close and the shutdown sequence cannot complete. By using -ForceRemove, we skip the service shutdown sequence and the service is removed ungracefully. To check if replicas are present, use [Get-ServiceFabricReplica](./Get-ServiceFabricReplica.md).

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
Specifies the Uniform Resource Identifier (URI) of a Service Fabric service.

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
This cmdlet accepts a URI that represents the name of a Service Fabric service.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricService](./Get-ServiceFabricService.md)

[New-ServiceFabricService](./New-ServiceFabricService.md)

[Resolve-ServiceFabricService](./Resolve-ServiceFabricService.md)

[Update-ServiceFabricService](./Update-ServiceFabricService.md)
