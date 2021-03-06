---
external help file: Microsoft.Open.AzureADBeta.Graph.PowerShell.dll-Help.xml
ms.assetid: B505822C-4BAA-4EC5-BB0A-128C093930C6
online version:
schema: 2.0.0
updated_at: 03/23/2017 02:03 AM
ms.date: 03/23/2017
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Add-AzureADScopedRoleMembership.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/Add-AzureADScopedRoleMembership.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/12dd31ac5269483f6fb3b8ef503a074c46e59754
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: carolz
---

# Add-AzureADScopedRoleMembership

## SYNOPSIS
Adds a scoped role membership to an administrative unit.

## SYNTAX

```
Add-AzureADScopedRoleMembership -ObjectId <String>
 [-RoleObjectId <String>] [-RoleMemberInfo <RoleMemberInfo>] [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADScopedRoleMembership cmdlet adds a scoped role membership to an administrative unit.

## EXAMPLES

### Example 1

```
	$User = Get-AzureADUser -SearchString "The user that will be an admin on this unit"
	$Role = Get-AzureADDirectoryRole | Where-Object -Property DisplayName -EQ -Value "User Account Administrator"
	$Unit = Get-AzureADAdministrativeUnit | Where-Object -Property DisplayName -Eq -Value "<The display name of the unit"
	$RoleMember = New-Object -TypeName Microsoft.Open.AzureAD.Model.RoleMemberInfo
	$RoleMember.ObjectId = $User.ObjectID
	Add-AzureADScopedRoleMembership -ObjectId $unit.ObjectId -RoleObjectId $Role.ObjectId -RoleMemberInfo $RoleMember
```
This cmdlet returns the Scope role membership object:
 

	AdministrativeUnitObjectId           RoleObjectId
	--------------------------           ------------
	c9ab56cc-e349-4237-856e-cab03157a91e 526b7173-5a6e-49dc-88ec-b677a9093709


## PARAMETERS

### -AdministrativeUnitObjectId
Specifies the ID of an admininstrative unit.

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

### -ObjectId
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -RoleMemberInfo
Specifies a **RoleMemberInfo** object. 
```yaml
Type: RoleMemberInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleObjectId
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADScopedRoleMembership](./Get-AzureADScopedRoleMembership.md)

[Remove-AzureADScopedRoleMembership](./Remove-AzureADScopedRoleMembership.md)

