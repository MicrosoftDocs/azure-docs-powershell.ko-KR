---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696787"
---
# Test-AzDataLakeStoreItem

## SYNOPSIS
Data Lake Store에서 파일 또는 폴더가 있는지 테스트 합니다.

## 구문과

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDataLakeStoreItem** Cmdlet은 Data Lake store에 파일 또는 폴더가 있는지 테스트 합니다.

## 예제의

### 예제 1: 파일 테스트
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

이 명령은 ContosoADL 계정에 파일 Test.csv 있는지 여부를 테스트 합니다.

## 변수

### -계정
Data Lake Store 계정의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -Path
루트 디렉터리 (/)로 시작 하 여 테스트할 항목의 Data Lake Store 경로를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PathType
테스트할 항목의 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 이상 
- 파일 
- 폴더

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### DataLakeStore. DataLakeStorePathInstance/.

### DataLakeStore/DataLakeStoreEnums + PathType (Microsoft.

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[Export-AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

[가져오기-AzDataLakeStoreItem](./Import-AzDataLakeStoreItem.md)

[참가-AzDataLakeStoreItem](./Join-AzDataLakeStoreItem.md)

[이동-AzDataLakeStoreItem](./Move-AzDataLakeStoreItem.md)

[제거-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)


