---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 11baabe406180e92a4a6af0f62b5e3b285e016b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700000"
---
# Set-AzLoadBalancerRuleConfig

## SYNOPSIS
부하 분산 장치에 대 한 규칙 구성을 업데이트 합니다.

## 구문과

### SetByResource (기본값)
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzLoadBalancerRuleConfig** cmdlet은 부하 분산 장치에 대 한 규칙 구성을 업데이트 합니다.

## 예제의

### 예제 1: 부하 분산 규칙 구성 수정
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.
두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 Add-AzLoadBalancerRuleConfig에 전달 하 여 NewRule 이라는 규칙을 추가 합니다.
세 번째 명령은 새 규칙 구성을 설정 하는 **AzLoadBalancerRuleConfig** 에 부하 분산을 전달 합니다.
이 구성은 이전 명령에서 사용 하도록 설정한 부동 IP 주소를 사용 하도록 설정 하지 않는다는 점에 유의 하세요.

## 변수

### -BackendAddressPool
부하 분산 장치 규칙과 연결할 **BackendAddressPool** 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendAddressPoolId
부하 분산 장치 규칙 구성과 연결할 **BackendAddressPool** 개체의 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackendPort
이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -DisableOutboundSNAT
부하 분산 규칙의 프런트 엔드에 지정 된 publicIP 주소를 사용 하도록 백 엔드 풀의 Vm에 대 한 SNAT를 구성 합니다.

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

### -EnableFloatingIP
이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.

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

### -EnableTcpReset
TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다. 이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.

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

### -FrontendIpConfiguration
부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FrontendIpConfigurationId
프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FrontendPort
부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancer
부하 분산 장치를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 규칙 구성을 업데이트 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -LoadDistribution
부하 분포를 지정 합니다.
이 매개 변수에 허용 되는 값은 SourceIP 및 SourceIPProtocol입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
부하 분산 장치의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로브
부하 분산 장치 규칙 구성과 연결할 프로브를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProbeId
부하 분산 장치 규칙 구성과 연결할 프로브 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로토콜
부하 분산 장치 규칙에 맞는 프로토콜을 지정 합니다.
이 매개 변수에 허용 되는 값은 Tcp 또는 Udp입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. 네트워크. PSLoadBalancer

### System. 문자열

### 시스템. i i.

### PSFrontendIPConfiguration에 대 한.

### PSBackendAddressPool에 대 한.

### Microsoft. 네트워크. PSProbe

## 출력

### Microsoft. 네트워크. PSLoadBalancer

## 상속자

## 관련 링크

[추가-AzLoadBalancerRuleConfig](./Add-AzLoadBalancerRuleConfig.md)

[추가-AzLoadBalancerRuleConfig](./Add-AzLoadBalancerRuleConfig.md)

[Get-AzLoadBalancerRuleConfig](./Get-AzLoadBalancerRuleConfig.md)

[새로운 AzLoadBalancerRuleConfig](./New-AzLoadBalancerRuleConfig.md)

[제거-AzLoadBalancerRuleConfig](./Remove-AzLoadBalancerRuleConfig.md)


