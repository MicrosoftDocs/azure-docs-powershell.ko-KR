---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523615"
---
# Get-AzsGalleryItem

## SYNOPSIS
갤러리 항목을 나열 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### 가져오기
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## 설명은
Azure Stack Marketplace에서 사용할 수 있는 갤러리 항목 목록 가져오기

## 예제의

### --------------------------예제 1--------------------------
```
Get-AzsGalleryItem
```

갤러리 항목을 나열 합니다.

### --------------------------예제 2--------------------------
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

이름으로 갤러리 항목을 가져옵니다.

## 변수

### -이름
갤러리 항목의 id입니다.
Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### Microsoft AzureStack. 관리자. 모델. m m a 관리

## 상속자

## 관련 링크

