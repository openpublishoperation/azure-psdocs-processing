---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 0A8D8356-C8A1-4EA7-9E0C-3C7A483EB72E
online version:
schema: 2.0.0
updated_at: Invalid date
ms.date: Invalid date
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/New-ServiceFabricServiceFromTemplate.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/New-ServiceFabricServiceFromTemplate.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# New-ServiceFabricServiceFromTemplate

## SYNOPSIS
If the application manifest has defined a service templates section, then this command can be used to create new services with service description parameters populated from the template. 

## SYNTAX

```
New-ServiceFabricServiceFromTemplate [-ApplicationName] <Uri> [-ServiceName] <Uri> [-ServiceTypeName] <String>
 [-Force] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
[New-ServiceFabricService](./New-ServiceFabricService.md) has several mandatory parameters that describe the service being created. Service templates in the application manifest can be used to specify service description parameters on a per service type basis. The service description schema in the service template section is the same as the service description schema for [default services](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model). This allows creating new services of a particular service type without specifying parameters that would otherwise have been mandatory for [New-ServiceFabricService](./New-ServiceFabricService.md).

Services created using a service template behave identically to services created using [New-ServiceFabricService](./New-ServiceFabricService). They can be upgraded, updated, and removed using the same workflows.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Create a service from a service template

Given the following application and service manifests:

```
<?xml version="1.0" encoding="utf-8" ?>
<ApplicationManifest
      ApplicationTypeName="MyApplicationType"
      ApplicationTypeVersion="AppManifestVersion1"
      xmlns="http://schemas.microsoft.com/2011/01/fabric"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <Description>An example application manifest</Description>
  <ServiceManifestImport>
    <ServiceManifestRef ServiceManifestName="MyServiceManifest" ServiceManifestVersion="SvcManifestVersion1"/>
  </ServiceManifestImport>
  <ServiceTemplates>
     <StatelessService ServiceTypeName="MyServiceType" InstanceCount="-1">
         <SingletonPartition/>
     </StatelessService>
  </ServiceTemplates>
</ApplicationManifest>

<?xml version="1.0" encoding="utf-8" ?>
<ServiceManifest Name="MyServiceManifest" Version="SvcManifestVersion1" xmlns="http://schemas.microsoft.com/2011/01/fabric" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <Description>An example service manifest</Description>
  <ServiceTypes>
    <StatelessServiceType ServiceTypeName="MyServiceType" />
  </ServiceTypes>
  <CodePackage Name="MyCode" Version="CodeVersion1">
    <EntryPoint>
      <ExeHost>
        <Program>MyServiceHost.exe</Program>
      </ExeHost>
    </EntryPoint>
  </CodePackage>
</ServiceManifest>
```

The following command creates a Service Fabric service using the service template for service type **MyServiceType** defined in the application manifest:



PS C:\>New-ServiceFabricServiceFromTemplate -ApplicationName fabric:/myapp -ServiceName fabric:/myapp/myservice1 -ServiceTypeName MyServiceType 


Multiple service instances can be created using the same service template. After additionally running the following command, there will be two singleton stateless services of type **MyServiceType**:


PS C:\>New-ServiceFabricServiceFromTemplate -ApplicationName fabric:/myapp -ServiceName fabric:/myapp/myservice2 -ServiceTypeName MyServiceType 


## PARAMETERS

### -ApplicationName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric application to create the service in.

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
Specifies the URI of a Service Fabric service.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTypeName
Specifies the name of a Service Fabric service type for which there is a service template defined in the application manifest.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### System.Object

This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[New-ServiceFabricService](./New-ServiceFabricService.md)

[Remove-ServiceFabricService](./Remove-ServiceFabricService.md)

[Update-ServiceFabricService](./Update-ServiceFabricService.md)
