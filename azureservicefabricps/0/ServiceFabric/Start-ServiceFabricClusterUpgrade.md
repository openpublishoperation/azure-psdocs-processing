---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
ms.assetid: 32BC7760-F639-4236-8F42-6C68ADE81F25
online version:
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricClusterUpgrade.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/service-fabric-cmdlets/ServiceFabric/vlatest/Start-ServiceFabricClusterUpgrade.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/
ms.topic: reference
author: oanapl
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
open_to_public_contributors: false
---

# Start-ServiceFabricClusterUpgrade

## SYNOPSIS
Upgrades a Service Fabric cluster.

## SYNTAX

### Both UnmonitoredAuto (Default)
```
Start-ServiceFabricClusterUpgrade [-CodePackageVersion] <String> [-ClusterManifestVersion] <String>
 [-ForceRestart] [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>]
 [-RestartProcess] [-UnmonitoredAuto] [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Code UnmonitoredAuto
```
Start-ServiceFabricClusterUpgrade [-Code] [-CodePackageVersion] <String> [-ForceRestart]
 [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>] [-RestartProcess]
 [-UnmonitoredAuto] [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Code Monitored
```
Start-ServiceFabricClusterUpgrade [-Code] [-CodePackageVersion] <String> [-ForceRestart]
 [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>] [-RestartProcess]
 [-Monitored] -FailureAction <UpgradeFailureAction> [-HealthCheckRetryTimeoutSec <UInt32>]
 [-HealthCheckWaitDurationSec <UInt32>] [-HealthCheckStableDurationSec <UInt32>]
 [-UpgradeDomainTimeoutSec <UInt32>] [-UpgradeTimeoutSec <UInt32>] [-ConsiderWarningAsError <Boolean>]
 [-MaxPercentUnhealthyApplications <Byte>] [-MaxPercentUnhealthyNodes <Byte>]
 [-ApplicationTypeHealthPolicyMap <ApplicationTypeHealthPolicyMap>] [-EnableDeltaHealthEvaluation]
 [-MaxPercentDeltaUnhealthyNodes <Byte>] [-MaxPercentUpgradeDomainDeltaUnhealthyNodes <Byte>] [-Force]
 [-ApplicationHealthPolicyMap <ApplicationHealthPolicyMap>] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Code UnmonitoredManual
```
Start-ServiceFabricClusterUpgrade [-Code] [-CodePackageVersion] <String> [-ForceRestart]
 [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>] [-RestartProcess]
 [-UnmonitoredManual] [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Config Monitored
```
Start-ServiceFabricClusterUpgrade [-Config] [-ClusterManifestVersion] <String> [-ForceRestart]
 [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>] [-RestartProcess]
 [-Monitored] -FailureAction <UpgradeFailureAction> [-HealthCheckRetryTimeoutSec <UInt32>]
 [-HealthCheckWaitDurationSec <UInt32>] [-HealthCheckStableDurationSec <UInt32>]
 [-UpgradeDomainTimeoutSec <UInt32>] [-UpgradeTimeoutSec <UInt32>] [-ConsiderWarningAsError <Boolean>]
 [-MaxPercentUnhealthyApplications <Byte>] [-MaxPercentUnhealthyNodes <Byte>]
 [-ApplicationTypeHealthPolicyMap <ApplicationTypeHealthPolicyMap>] [-EnableDeltaHealthEvaluation]
 [-MaxPercentDeltaUnhealthyNodes <Byte>] [-MaxPercentUpgradeDomainDeltaUnhealthyNodes <Byte>] [-Force]
 [-ApplicationHealthPolicyMap <ApplicationHealthPolicyMap>] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Config UnmonitoredAuto
```
Start-ServiceFabricClusterUpgrade [-Config] [-ClusterManifestVersion] <String> [-ForceRestart]
 [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>] [-RestartProcess]
 [-UnmonitoredAuto] [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Config UnmonitoredManual
```
Start-ServiceFabricClusterUpgrade [-Config] [-ClusterManifestVersion] <String> [-ForceRestart]
 [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>] [-RestartProcess]
 [-UnmonitoredManual] [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Both Monitored
```
Start-ServiceFabricClusterUpgrade [-CodePackageVersion] <String> [-ClusterManifestVersion] <String>
 [-ForceRestart] [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>]
 [-RestartProcess] [-Monitored] -FailureAction <UpgradeFailureAction> [-HealthCheckRetryTimeoutSec <UInt32>]
 [-HealthCheckWaitDurationSec <UInt32>] [-HealthCheckStableDurationSec <UInt32>]
 [-UpgradeDomainTimeoutSec <UInt32>] [-UpgradeTimeoutSec <UInt32>] [-ConsiderWarningAsError <Boolean>]
 [-MaxPercentUnhealthyApplications <Byte>] [-MaxPercentUnhealthyNodes <Byte>]
 [-ApplicationTypeHealthPolicyMap <ApplicationTypeHealthPolicyMap>] [-EnableDeltaHealthEvaluation]
 [-MaxPercentDeltaUnhealthyNodes <Byte>] [-MaxPercentUpgradeDomainDeltaUnhealthyNodes <Byte>] [-Force]
 [-ApplicationHealthPolicyMap <ApplicationHealthPolicyMap>] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Both UnmonitoredManual
```
Start-ServiceFabricClusterUpgrade [-CodePackageVersion] <String> [-ClusterManifestVersion] <String>
 [-ForceRestart] [[-UpgradeReplicaSetCheckTimeoutSec] <UInt32>] [-ReplicaQuorumTimeoutSec <UInt32>]
 [-RestartProcess] [-UnmonitoredManual] [-Force] [-TimeoutSec <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Start-ServiceFabricClusterUpgrade** cmdlet upgrades a Service Fabric cluster.
You can upgrade Service Fabric code, configuration, or both code and configuration.

To manage Service Fabric clusters, start Windows PowerShell by using the Run as administrator option.
Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the [Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md) cmdlet.

## EXAMPLES

### Example 1: Start unmonitored manual upgrade
```
PS C:\>Start-ServiceFabricClusterUpgrade -CodePackageVersion "2.0.59.0" -ClusterManifestVersion "v2" -UnmonitoredManual
```

This command starts the unmonitored manual upgrade for the specified code package and configuration.

### Example 2: Start upgrade for code only
```
PS C:\>Start-ServiceFabricClusterUpgrade -Code -CodePackageVersion "2.0.59.0" -UnmonitoredAuto
```

This command starts the unmonitored automatic upgrade for the specified code package.
There is no configuration upgrade.

### Example 3: Start config only upgrade
```
Start-ServiceFabricClusterUpgrade -ClusterManifestVersion "v2" -Config -FailureAction Rollback -Monitored
```

This command starts the monitored config only upgrade for the specified cluster manifest version. The upgrade uses default health policies and the failure action is specified as *Rollback*.

### Example 4: Start upgrade with a custom health policy
```
PS C:\>$AppTypeHealthPolicyMap = New-Object -TypeName "System.Fabric.Health.ApplicationTypeHealthPolicyMap"
PS C:\> $AppTypeHealthPolicyMap.Add("CriticalAppType", 0)

PS C:\> $svcType = New-Object -TypeName System.Fabric.Health.ServiceTypeHealthPolicy
PS C:\> $svcType.MaxPercentUnhealthyPartitionsPerService = 20
PS C:\> $svcType.MaxPercentUnhealthyReplicasPerPartition = 20
PS C:\> $warningAsErrorPolicy = New-Object -TypeName System.Fabric.Health.ApplicationHealthPolicy
PS C:\> $warningAsErrorPolicy.ConsiderWarningAsError = $true
PS C:\> $warningAsErrorPolicy.DefaultServiceTypeHealthPolicy = $svcType

PS C:\> $appHealthPolicyMap = New-Object -TypeName System.Fabric.Health.ApplicationHealthPolicyMap
PS C:\> $appHealthPolicyMap.Add("fabric:/System", $warningAsErrorPolicy)

PS C:\> Start-ServiceFabricClusterUpgrade -CodePackageVersion "4.2.83.9493" -ClusterManifestVersion "ScaleMin-1.0" -Monitored -FailureAction Rollback -ApplicationTypeHealthPolicyMap $AppTypeHealthPolicyMap -Force -MaxPercentUnhealthyNodes 20 -MaxPercentUnhealthyApplications 20 -ApplicationHealthPolicyMap $appHealthPolicyMap
```

This command starts the monitored upgrade for the specified code package and configuration and passes custom health policies.
It specifies a custom cluster health policy, defines a different MaxPercentUnhealthyApplications for a critical application type and a custom application health policy for the cluster System application.

## PARAMETERS

### -ApplicationHealthPolicyMap
Specifies a **System.Fabric.Health.ApplicationHealthPolicyMap** object that includes custom health policies for some or all of the applications.
If you do not specify this parameter, or if you don't include an entry in the map for an application, that application is evaluated with the application health policy defined in the application manifest if it exists, or the default health policy otherwise.

```yaml
Type: ApplicationHealthPolicyMap
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationTypeHealthPolicyMap
Specifies the map that defines the maximum percentage of unhealthy applications that are allowed per application type.
Application types in this map are evaluated using specific percentages rather than the global percentage specified in the *MaxPercentUnhealthyApplications* parameter.

For example, if some applications of a type are critical, the cluster administrator can add an entry to the map for that application type and assign it a value of 0% (that is, do not tolerate any failures).
All other applications can be evaluated with the *MaxPercentUnhealthyApplications* parameter set to 20% to tolerate some failures out of the thousands of application instances.

The application type health policy map is used only if the cluster manifest enables application type health evaluation using the configuration entry for **HealthManager/EnableApplicationTypeHealthEvaluation**.

```yaml
Type: ApplicationTypeHealthPolicyMap
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterManifestVersion
Specifies the version stored in a Service Fabric cluster manifest.

```yaml
Type: String
Parameter Sets: Both UnmonitoredAuto, Config Monitored, Config UnmonitoredAuto, Config UnmonitoredManual, Both Monitored, Both UnmonitoredManual
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Code
Indicates that the package includes only a Service Fabric .msi file.

```yaml
Type: SwitchParameter
Parameter Sets: Code UnmonitoredAuto, Code Monitored, Code UnmonitoredManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CodePackageVersion
Specifies the version of the Service Fabric .msi file.

```yaml
Type: String
Parameter Sets: Both UnmonitoredAuto, Code UnmonitoredAuto, Code Monitored, Code UnmonitoredManual, Both Monitored, Both UnmonitoredManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Indicates that the package is a Service Fabric cluster manifest.

```yaml
Type: SwitchParameter
Parameter Sets: Config Monitored, Config UnmonitoredAuto, Config UnmonitoredManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts for confirmation before running the cmdlet.

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

### -ConsiderWarningAsError
Indicates whether to treat a warning health event as an error event during health evaluation of the cluster entity and of the Nodes entities.
Applications are evaluated using per application health policy settings.

```yaml
Type: Boolean
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDeltaHealthEvaluation
Indicates that delta health evaluation is used to determine if the Service Fabric cluster is healthy.

```yaml
Type: SwitchParameter
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailureAction
Specifies the action to take if the monitored upgrade fails.
The acceptable values for this parameter are:

- Rollback
- Manual

```yaml
Type: UpgradeFailureAction
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 
Accepted values: Invalid, Rollback, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indicates that this cmdlet skips the warning message and forces the upgrade.

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

### -ForceRestart
Indicates that the service host restarts even if the upgrade is a configuration-only change.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HealthCheckRetryTimeoutSec
Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.

```yaml
Type: UInt32
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HealthCheckStableDurationSec
Specifies the duration, in seconds, that Service Fabric waits in order to verify that the cluster is stable before moving to the next upgrade domain or completing the upgrade.
This wait duration prevents undetected changes of health right after the health check is performed.

```yaml
Type: UInt32
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HealthCheckWaitDurationSec
Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.

```yaml
Type: UInt32
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPercentDeltaUnhealthyNodes
Specifies the maximum percentage of delta unhealthy nodes that can have aggregated health states of error.
If the current unhealthy nodes do not respect the percentage relative to the state at the beginning of the upgrade, the cluster is considered unhealthy.

```yaml
Type: Byte
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPercentUnhealthyApplications
Specifies the maximum percentage of applications that can have aggregated health states of error.
If the currently unhealthy applications do not respect this amount, the cluster is considered unhealthy.

```yaml
Type: Byte
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPercentUnhealthyNodes
Specifies the maximum percentage of nodes that can have aggregated health states of error.
If the current unhealthy applications do not respect this percentage, the cluster is considered unhealthy.

```yaml
Type: Byte
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPercentUpgradeDomainDeltaUnhealthyNodes
Specifies the maximum percentage of upgrade domain delta unhealthy nodes that can have aggregated health states of error.
If there is any upgrade domain where the current unhealthy nodes do not respect the percentage relative to the state at the beginning of the upgrade, the cluster is considered unhealthy.

```yaml
Type: Byte
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Monitored
Indicates that the upgrade mode is monitored.
This means that health checks are performed after upgrade finishes for an upgrade domain. If the health of the upgrade domain and the cluster meet the specified health policies, Service Fabric starts upgrade of the next upgrade domain.
If the upgrade domain or cluster fails to meet health policies, the upgrade fails and Service Fabric rolls back the upgrade or switches to unmonitored manual mode, depending on the specified *FailureAction*.

```yaml
Type: SwitchParameter
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaQuorumTimeoutSec
Specifies the time-out period, in seconds, to check whether the replica set has quorum.
After the time out period, the upgrade proceeds.

This parameter has been deprecated.
Specify the *UpgradeReplicaSetCheckTimeoutSec* parameter instead.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartProcess
Indicates that the service host restarts as part of the upgrade.

This parameter has been deprecated.
Specify the *ForceRestart* parameter instead.

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

### -UnmonitoredAuto
Indicates that the upgrade mode is unmonitored automatic.
No health checks are performed and after Service Fabric upgrades an upgrade domain, Service Fabric starts the upgrade of the next upgrade domain irrespective of the cluster health state.
This mode is not recommended for production use.

```yaml
Type: SwitchParameter
Parameter Sets: Both UnmonitoredAuto, Code UnmonitoredAuto, Config UnmonitoredAuto
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnmonitoredManual
Indicates that the upgrade mode is unmonitored manual.
After Service Fabric upgrades an upgrade domain, it waits for the [Resume-ServiceFabricClusterUpgrade](./Resume-ServiceFabricClusterUpgrade.md) cmdlet to explicitly start the upgrade of the next upgrade domain.

```yaml
Type: SwitchParameter
Parameter Sets: Code UnmonitoredManual, Config UnmonitoredManual, Both UnmonitoredManual
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeDomainTimeoutSec
Specifies the maximum time, in seconds, that Service Fabric can take to upgrade a single upgrade domain.
After this period, the upgrade fails.

```yaml
Type: UInt32
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeReplicaSetCheckTimeoutSec
Specifies the maximum time that Service Fabric waits for a partition to be in a safe state, if not already in a safe state. Once safety checks pass for all partitions on a node, Service Fabric proceeds with the upgrade on that node.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeTimeoutSec
Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.
After this period, the upgrade fails.

```yaml
Type: UInt32
Parameter Sets: Code Monitored, Config Monitored, Both Monitored
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
The cmdlet is not run.

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

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns a **System.Fabric.Description.FabricUpgradeDescription** for a Service Fabric cluster upgrade.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricClusterUpgrade](./Get-ServiceFabricClusterUpgrade.md)

[Update-ServiceFabricClusterUpgrade](./Update-ServiceFabricClusterUpgrade)

[Resume-ServiceFabricClusterUpgrade](./Resume-ServiceFabricClusterUpgrade.md)

[Remove-ServiceFabricClusterPackage](./Remove-ServiceFabricClusterPackage.md)
