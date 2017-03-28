---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 4290C7C9-446B-4A8F-BD52-5E2508700FFC
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/New-ServiceFabricNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/New-ServiceFabricNodeConfiguration.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# New-ServiceFabricNodeConfiguration

## SYNOPSIS
Configures a node to join a Service Fabric cluster. Works for development clusters and Azure clusters.

## SYNTAX

```
New-ServiceFabricNodeConfiguration [-ClusterManifestPath] <String> [-InfrastructureManifestPath <String>]
 [-FabricDataRoot <String>] [-FabricLogRoot <String>] [-FabricHostCredential <PSCredential>]
 [-RunFabricHostServiceAsManual] [-RemoveExistingConfiguration] [-BootstrapMSIPath <String>]
 [-UsingFabricPackage] [-FabricPackageRoot <String>] [-MachineName <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-ServiceFabricNodeConfiguration** cmdlet configures a node to be able to be added to a Service Fabric cluster. This involves installing Service Fabric if required, and then using configuration information taken from the cluster manifest and then creates the settings required for the node to join the cluster.

The node will join the cluster as soon as the Service Fabric Host Service is started on the host machine.

To manage Service Fabric clusters make sure you start your Windows PowerShell session by using the Run as administrator option.

This command will have different usages of parameters depending on the type of cluster this operation is applied to. In all cases, this command is used to add a node to a cluster. If using a standalone cluster, please refer to the [AddNode](/azure/service-fabric/service-fabric-cluster-windows-server-add-remove-nodes.md) command.

## EXAMPLES

### Example 1: Configure a five-node development cluster
```
PS C:\>New-ServiceFabricNodeConfiguration -ClusterManifestPath "<samples>\\ConfigStore\Management\Deployment\ClusterManifest\Server\DevEnv-FiveNodes.xml"
```

This command configures a development cluster by using the DevEnv-FiveNodes.xml manifest from the Service Fabric samples.
That manifest configures a Service Fabric cluster of five nodes on your development computer.

## PARAMETERS

### -BootstrapMSIPath
Specifies the path of the bootstrap .msi file. This is the Service Fabric SDK downloaded from the Service Fabric website.
If you use this parameter, a self-baseline upgrade automatically occurs, either when an upgrade is configured or fabric is upgraded.
If -UsingFabricPackage is set, this should point to the Service Fabric CAB file rather than the .msi file. The Service Fabric CAB file is available for download [here](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation.md).

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

### -ClusterManifestPath
Specifies the path of a Service Fabric cluster manifest, which is an XML file. Samples of this file can be seen in [Service Fabric samples](https://github.com/Azure-Samples/service-fabric-dotnet-getting-started) under "PublishProfiles".
The cmdlet creates a cluster configuration based on the specified manifest.

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

### -FabricDataRoot
Specifies the path where the Service Fabric runtime stores the internal data needed to operate a cluster.

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

### -FabricHostCredential
Specifies a **PSCredential** object for the Service Fabric Host Service.
To obtain a **PSCredential** object, use the [Get-Credential](http://go.microsoft.com/fwlink/?LinkID=293936) cmdlet.
For more information, type `Get-Help Get-Credential`.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FabricLogRoot
Specifies the path for the Service Fabric trace logs.

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

### -FabricPackageRoot
This parameter is reserved for future use.

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

### -InfrastructureManifestPath
Specifies the path of the infrastructure manifest. This manifest is used to give each node an overview of the cluster. For example, the total amount of nodes on the cluster.
In Azure, this is the path to the .csdef and .cscfg files.

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

### -MachineName
Specifies the computer that will host the configuration.
You can use either the computer name or the computer IP address.
For example:

`-MachineName "192.168.1.1"`

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

### -RemoveExistingConfiguration
Indicates that this cmdlet removes any existing configurations. These configurations consist of data found in the folders pointed by FabricDataRoot and FabricLogRoot.

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

### -RunFabricHostServiceAsManual
Indicates that the Fabric Host service must be started manually.

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

### -UsingFabricPackage
Indicates that node configurations should use the xcopy/CAB runtime package. This can be downloaded from the Service Fabric website.
This is used when MSI is not installed and we are using a client package to execute the cmdlet. The path to the xcopy/CAB package should be set in the parameter -BootstrapMSIPath.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

###  
**New-ServiceFabricNodeConfiguration** does not accept pipelined input.

## OUTPUTS

###  
**New-ServiceFabricNodeConfiguration** returns the status of this operation as a string value. This can be an error message.

## NOTES

## RELATED LINKS

[Get-Credential](http://go.microsoft.com/fwlink/?LinkID=293936)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Remove-ServiceFabricNodeConfiguration](./Remove-ServiceFabricNodeConfiguration.md)

[Update-ServiceFabricNodeConfiguration](./Update-ServiceFabricNodeConfiguration.md)
