---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 1F3E9453-D4DA-47A0-B7D5-E2D9110D382A
updated_at: 03/27/2017 18:03 PM
ms.date: 03/27/2017
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/Azure.Storage/v2.1.0/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/Azure.Storage/v2.1.0/Get-AzureStorageFile.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/9b79c0a37330eb2c43d3e7d31b5ab53f0da9554c
ms.topic: reference
author: erickson-doug
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: erickson-doug
open_to_public_contributors: false
---

# Get-AzureStorageFile

## SYNOPSIS
Lists directories and files for a path.

## SYNTAX

### ShareName (Default)
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <AzureStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-PipelineVariable <String>]
 [<CommonParameters>]
```

### Share
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-PipelineVariable <String>] [<CommonParameters>]
```

### Directory
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-PipelineVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.
Specify the *Path* parameter to get an instance of a directory or file in the specified path.

This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.
You can use the **IsDirectory** property to distinguish between folders and files.

## EXAMPLES

### Example 1: List directories in a share
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

This command lists only the directories in the share ContosoShare06.
It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".

### Example 2: List a File Directory
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06"  -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.
It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.

## PARAMETERS

### -ShareName
Specifies the name of the file share.
This cmdlet gets a file or directory from the file share that this parameter specifies.

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
Specifies the path of a folder.

If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.
If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Specifies an Azure Storage context.
To obtain a Storage context, use the New-AzureStorageContext cmdlet.

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
Specifies the service-side timeout interval, in seconds, for a request.
If the specified interval elapses before the service processes the request, the Storage service returns an error.

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
Specifies the client side time-out interval, in seconds, for one service request.
If the previous call fails within the specified interval, this cmdlet retries the request.
If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.

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
Specifies the maximum concurrent network calls.
You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.
The specified value is an absolute count and is not multiplied by the core count.
This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.
The default value is 10.

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

### -Share
Specifies a **CloudFileShare** object.
This cmdlet gets a file or directory from the file share that this parameter specifies.
To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.
This object contains the Storage context.
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
This cmdlet gets the folder that this parameter specifies.
To obtain a directory, use the New-AzureStorageDirectory cmdlet.
You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.

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

[Get-AzureStorageFileContent](./Get-AzureStorageFileContent.md)

[New-AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)

[Remove-AzureStorageFile](./Remove-AzureStorageFile.md)

[Set-AzureStorageFileContent](./Set-AzureStorageFileContent.md)
