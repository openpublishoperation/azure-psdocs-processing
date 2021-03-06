---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
online version:
schema: 2.0.0
updated_at: 03/15/2017 20:03 PM
ms.date: 03/15/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Sql/v2.7.0/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Sql/v2.7.0/Add-AzureRmSqlDatabaseToFailoverGroup.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/d661156ea7c515a4c8b6df33e68d65d50d6e9950
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Add-AzureRmSqlDatabaseToFailoverGroup

## SYNOPSIS
Cmdlet that adds databases into the Azure SQL Failover Group

## SYNTAX

```
Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName <String>
 -Databases <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Tags <Hashtable>] -ServerName <String> -ResourceGroupName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Cmdlet to add Azure Sql Databases into a Failover Group. Database input parameters should be a Azure Sql Database Model object, which could be obtained either through pipelining or storing in Powershell environment variables with the Get_AzureRmSqlDatabase Cmdelet. 

## EXAMPLES

### Example 1
```
PS C:\> Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName myFg-ResourceGroupName myRg -ServerName mysvr
```

### Example 2
```
Using Pipe Line to pipe in the database objects 

PS C:\> Get-AzureRmSqlDatabase -ServerName testsvr -ResourceGroupName rg2 | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName myFg-ResourceGroupName myRg -ServerName mysvr
```


## PARAMETERS

### -Databases
The Azure SQL Databases to be added to the secondary server.```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FailoverGroupName
The name of the Azure SQL Failover Group.```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group.```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
The name of the Azure SQL Server the Failover Group is in.```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
The tags to associate with the Azure Sql Elastic Pool```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

