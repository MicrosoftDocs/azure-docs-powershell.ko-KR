---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 65825e1cbb5da41d1557d30b0f152ee456e6e86b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532115"
---
# Set-AzureRmApplicationGatewayProbeConfig

## SYNOPSIS
기존 응용 프로그램 게이트웨이에서 상태 프로브 구성을 설정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Set-AzureRmApplicationGatewayProbeConfig cmdlet은 기존 응용 프로그램 게이트웨이에서 상태 프로브 구성을 설정 합니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이에서 상태 프로브에 대 한 구성 설정
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 대 한 Probe05 이라는 상태 프로브에 대 한 구성을 설정 합니다.
또한이 명령은 비정상 임계값을 8 번 재시도로 설정 하 고 120 초 후에 시간 초과 합니다.

## 변수

### -ApplicationGateway
이 cmdlet이 프로브를 보내는 응용 프로그램 게이트웨이를 지정 합니다.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostName
이 cmdlet이 프로브를 보내는 호스트 이름을 지정 합니다.

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

### -Interval
검색 간격 (초)을 지정 합니다.
두 연속 프로브 간의 시간 간격입니다.
이 값의 범위는 1 초에서 86400 초 사이입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Match
상태 응답에 포함 해야 하는 본문입니다.
Default 값이 비어 있습니다.

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinServers
항상 정상 상태로 표시 된 최소 서버 수입니다.
기본값은 0입니다.

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

### -이름
프로브의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
프로브에 대 한 상대 경로를 지정 합니다.
유효한 경로는 슬래시 문자 (/)로 시작 합니다.
프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PickHostNameFromBackendHttpSettings
백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부
기본값은 false입니다.

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

### -프로토콜
프로브 전송에 사용 되는 프로토콜을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -시간 제한
프로브 시간 제한을 초 단위로 지정 합니다.
이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.
유효한 값의 범위는 1 초에서 86400 초입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnhealthyThreshold
프로브 재시도 횟수를 지정 합니다.
연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.
유효한 값의 범위는 1 초에서 20 초 사이입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSApplicationGateway
' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[추가-AzureRmApplicationGatewayProbeConfig]()

[Get-AzureRmApplicationGatewayProbeConfig]()

[새로운 AzureRmApplicationGatewayProbeConfig]()

[제거-AzureRmApplicationGatewayProbeConfig]()

