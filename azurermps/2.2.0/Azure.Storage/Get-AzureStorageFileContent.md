---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 2A8AF9CB-BCF9-4F57-94DC-053E9021FD9B
updated_at: 03/27/2017 18:03 PM
ms.date: 03/27/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/Azure.Storage/v2.1.0/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/Azure.Storage/v2.1.0/Get-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/9b79c0a37330eb2c43d3e7d31b5ab53f0da9554c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureStorageFileContent

## SYNOPSIS
Downloads the contents of a file.

## SYNTAX

### ShareName (Default)
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <AzureStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-PipelineVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Share
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-PipelineVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Directory
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-PipelineVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### File
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-PipelineVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.
This cmdlet does not return the contents of the file.

## EXAMPLES

### Example 1: Download a file from a folder
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.

## PARAMETERS

### -ShareName
Specifies the name of the file share.
This cmdlet downloads the contents of the file in the share this parameter specifies.

```yaml
Type: String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the path of a file.
This cmdlet gets the contents the file that this parameter specifies.
If the file does not exist, this cmdlet returns an error.

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destination
Specifies the destination path.
This cmdlet downloads the file contents to the location that this parameter specifies.

If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMd5
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

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

### -PassThru
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

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

### -Force
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

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

### -Context
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

```yaml
Type: AzureStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

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

### -ClientTimeoutPerRequest
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

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

### -ConcurrentTaskCount
If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.
If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.
If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.

If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.

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

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are:
* Continue
* Ignore
* Inquire
* SilentlyContinue
* Stop
* Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
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

### -Share
Specifies a **CloudFileShare** object.
This cmdlet downloads the contents of the file in the share this parameter specifies.
To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.
This object contains the storage context.
If you specify this parameter, do not specify the *Context* parameter.

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Directory
Specifies a folder as a **CloudFileDirectory** object.
This cmdlet gets content for a file in the folder that this parameter specifies.
To obtain a directory, use the New-AzureStorageDirectory cmdlet.
You can also use the Get-AzureStorageFile cmdlet to obtain a directory.

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -File
Specifies a file as a **CloudFile** object.
This cmdlet gets the file that this parameter specifies.
To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.

```yaml
Type: CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PipelineVariable
Stores the value of the current pipeline element as a variable, for any named command as it flows through the pipeline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: pv

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

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)
