---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 6e86ed8cde1297af54ffaf8f8c8fbc912da30e69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981072"
---
# Add-AzVhd

## SYNOPSIS
Azure의 클라우드 저장소 계정의 Blob에 온라인 가상 머신에서 가상 하드 디스크를 업로드합니다.

## 구문

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzVhd** cmdlet은 .vhd 파일 형식으로 프레미스 가상 하드 디스크를 고정된 가상 하드 디스크로 Blob Storage 계정에 업로드합니다.
사용할 업로더 스레드 수를 구성하거나 지정된 대상 URI에서 기존 Blob을 덮어 덮을 수 있습니다.
또한 지원되는 것은 패치된 버전의 On-Premises .vhd 파일을 업로드하는 능력입니다.
기본 가상 하드 디스크가 이미 업로드된 경우 기본 이미지를 부모로 사용하는 다른 디스크를 업로드할 수 있습니다.
SAS(공유 액세스 서명) URI도 지원됩니다.

## 예제

### 예제 1: VHD 파일 추가
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

이 명령은 저장소 계정에 .vhd 파일을 추가합니다.

### 예제 2: VHD 파일 추가 및 대상 덮어 사용
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

이 명령은 저장소 계정에 .vhd 파일을 추가합니다.
명령은 기존 파일을 덮어 덮어 덮어 니다.

### 예제 3: VHD 파일 추가 및 스레드 수 지정
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

이 명령은 저장소 계정에 .vhd 파일을 추가합니다.
명령은 파일을 업로드하는 데 사용할 스레드 수를 지정합니다.

### 예제 4: VHD 파일 추가 및 SAS URI 지정
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

이 명령은 저장소 계정에 .vhd 파일을 추가하고 SAS URI를 지정합니다.

## 매개 변수

### -AsJob
백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BaseImageUriToPatch
Azure Blob Storage의 기본 이미지 Blob에 URI를 지정합니다.
SAS를 이 매개 변수의 값으로 지정할 수 있습니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -대상
Blob Storage에서 Blob의 URI를 지정합니다.
매개 변수는 SAS URI를 지원하고, 패치 시나리오 대상은 SAS URI일 수 없습니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
로컬 .vhd 파일의 경로를 지정합니다.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
.vhd 파일을 업로드할 때 사용할 업로더 스레드 수를 지정합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
이 cmdlet이 있는 경우 지정된 대상 URI에 기존 Blob을 덮어 던지는 것을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Uri

### System.IO.FileInfo

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.Compute.Models.VhdUploadContext

## 참고 사항

## 관련 링크

[Save-AzVhd](./Save-AzVhd.md)


