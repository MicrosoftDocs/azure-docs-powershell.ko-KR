---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047391"
---
# Get-WAPackVMTemplate

## SYNOPSIS
가상 컴퓨터 템플릿을 가져옵니다.

## 구문과

### 비어 있음 (기본값)
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 찡그린 Mid
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**Get-WAPackVMTemplate** cmdlet은 가상 컴퓨터 템플릿을 가져옵니다.

## 예제의

### 예제 1: 이름을 사용 하 여 가상 컴퓨터 서식 파일 가져오기
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

이 명령은 ContosoTemplate04 이라는 가상 컴퓨터 템플릿을 가져옵니다.

### 예제 2: ID를 사용 하 여 가상 컴퓨터 서식 파일 가져오기
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

이 명령은 지정 된 ID를 가진 가상 컴퓨터 템플릿을 가져옵니다.

### 예제 3: 모든 가상 컴퓨터 템플릿 가져오기
```
PS C:\> Get-WAPackVMTemplate
```

이 명령은 모든 가상 컴퓨터 템플릿을 가져옵니다.

## 변수

### -ID
서식 파일의 고유 ID를 지정 합니다.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
서식 파일의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-WAPackVM](./Get-WAPackVM.md)


