---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 7556a2d23d4c4969c3037d6b49dbd482bcdea207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964112"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
이 명령을 사용하면 사용자가 IPsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하는 VPN ipsec 정책 개체를 만들 수 있습니다. 이 명령 let output 개체는 새/기존 게이트웨이 모두에 대한 vpn ipsec 정책을 설정하는 데 사용됩니다.

## 구문

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
이 명령을 사용하면 사용자가 IPsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하는 VPN ipsec 정책 개체를 만들 수 있습니다. 이 명령 let output 개체는 새/기존 게이트웨이 모두에 대한 vpn ipsec 정책을 설정하는 데 사용됩니다.

## 예제

### 예제 1: vpn ipsec 정책 개체 정의:
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

이 cmdlet은 사용자가 param:VPNClientIpsecPolicy의 param:vpnClientIpsecPolicy에 전달할 수 있는 하나 또는 모든 매개 변수 값을 사용하여 vpn ipsec 정책 개체를 만드는 데 사용됩니다. ResourceGroup에서 New-AzVirtualNetworkGateway(새 VPN 게이트웨이 만들기) / Set-AzVirtualNetworkGateway(기존 VPN Gateway 업데이트) :

### 예제 2: VPN 사용자 지정 ipsec 정책을 설정하여 새 가상 네트워크 게이트웨이 만들기:
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

이 cmdlet은 가상 네트워크 게이트웨이 개체를 생성한 후 반환합니다. 

### 예제 3: 기존 가상 네트워크 게이트웨이에서 VPN 사용자 지정 ipsec 정책을 설정합니다.
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

이 cmdlet은 VPN 사용자 지정 ipsec 정책을 설정한 후 가상 네트워크 게이트웨이 개체를 반환합니다.

### 예제 4: 가상 네트워크 게이트웨이를 사용하여 VPN 사용자 지정 정책이 올바르게 설정되어 있는지 확인합니다.
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

이 cmdlet은 가상 네트워크 게이트웨이 개체를 반환합니다.

## 매개 변수

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

### -DhGroup
초기 SA에 대한 IKE 1단계에서 사용되는 VpnClient DH 그룹

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
VpnClient IKE 암호화 알고리즘(IKE 2단계)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
VpnClient IKE 무결성 알고리즘(IKE 2단계)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
VpnClient IPSec 암호화 알고리즘(IKE 1단계)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
VpnClient IPSec 무결성 알고리즘(IKE 1단계)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
새 자식 SA에 대한 IKE 2단계에서 사용되는 VpnClient PFS 그룹

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
KB의 VpnClient IPSec 보안 협회(빠른 모드 또는 2단계 SA라고도 하는) 페이로드 크기

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
VpnClient IPSec 보안 협회(빠른 모드 또는 2단계 SA라고도 하는) 수명이 몇 초 만에

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy

## 참고 사항

## 관련 링크
