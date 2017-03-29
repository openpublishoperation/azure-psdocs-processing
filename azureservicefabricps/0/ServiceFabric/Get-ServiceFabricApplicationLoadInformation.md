---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 5960F91D-BFD2-4297-B7BE-5A325BCDEA0A
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationLoadInformation.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationLoadInformation.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: vipulm
open_to_public_contributors: false
---

# Get-ServiceFabricApplicationLoadInformation

## SYNOPSIS
Gets application capacity parameters and load information for a Service Fabric application.

## SYNTAX

```
Get-ServiceFabricApplicationLoadInformation [-ApplicationName] <String> [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricApplicationLoadInformation** cmdlet gets application capacity parameters and load information for a Service Fabric application.

The output of **Get-ServiceFabricApplicationLoadInformation** contains the following information: 

- Minimum Nodes: Minimum number of nodes specified for this application (from **Application Capacity** parameters). 
- Maximum Nodes: Maximum number of nodes specified for this application (from **Application Capacity** parameters). 
- Node Count: Number of nodes currently spanned by the application's child replicas. 
- Application Load Metric Information: Load information for each metric defined in **Application Capacity** parameters. 
For each metric that is defined, the output contains the following information: 
- Metric Name: Name of the metric. 
- Reservation Capacity: Cluster capacity that is reserved in the cluster for this application. 
- Application Load: Total Load of this application's child replicas. 
- Application Capacity: Maximum permitted value of Application Load.

## EXAMPLES

### Example 1: Get load information
```
PS C:\>Get-ServiceFabricApplicationLoadInformation -ApplicationName fabric:/MyApp
```

This command gets load information for the application fabric://MyApp.

## PARAMETERS

### -ApplicationName
Specifies a Service Fabric application.

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

## OUTPUTS

### System.Fabric.Query.ApplicationLoadInformation

## NOTES

## RELATED LINKS

[Get-ServiceFabricClusterLoadInformation](./Get-ServiceFabricClusterLoadInformation.md)

[Get-ServiceFabricNodeLoadInformation](./Get-ServiceFabricNodeLoadInformation.md)

[Get-ServiceFabricPartitionLoadInformation](./Get-ServiceFabricPartitionLoadInformation.md)


