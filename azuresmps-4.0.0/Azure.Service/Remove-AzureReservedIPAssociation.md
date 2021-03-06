---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046136"
---
# Remove-AzureReservedIPAssociation

## SYNOPSIS
예약 된 IP 주소에서 VM 또는 클라우드 서비스로의 연결을 제거 합니다.

## 구문과

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
AzureReservedIPAssociation cmdlet은 VM (가상 머신) 또는 클라우드 서비스에서 예약 된 IP 주소를 **분리** 합니다.
작업이 완료 되 면 예약 된 IP 주소는 무료이 고 VM/VIP는 Azure 인벤토리에서 동적 공용 IP 주소를 가져옵니다.

## 예제의

### 예제 1: 예약 된 IP 연결 제거
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

이 명령은 PipTestWestEurope 이라는 서비스에서 ResIp14 이라는 예약 된 IP 주소를 분리 합니다.
PipTestWestEurope에 새 동적 VIP가 할당 됩니다.

## 변수

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

이 플래그를 사용 하 여 예약 된 IP 연결을 제거할 때 경고 메시지를 무시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

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
정보 변수를 지정 합니다.

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

### -ReservedIPName
예약 된 IP 주소의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
배포 환경을 지정 합니다.
이 매개 변수에 허용 되는 값은 프로덕션, 스테이징입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualIPName
서비스 또는 VM과의 연결을 제거할 가상 IP 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure. 유틸리티. ManagementOperationContext

## 상속자

## 관련 링크

[Set-AzureReservedIPAssociation](./Set-AzureReservedIPAssociation.md)


