---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: b72b072307ee4d8ae304888e2d1b3db4a36be3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202476"
---
# Set-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
프런트 엔드 IP 주소 구성을 수정합니다.

## 구문

### SetByResourceId
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-PrivateLinkConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzApplicationGatewayFrontendIPConfig** cmdlet은 프런트 엔드 IP 구성을 업데이트합니다.
애플리케이션 게이트웨이는 두 가지 유형의 프런트 엔드 IP 주소를 지원합니다. 
- 공용 IP 주소
- 구성에서 ILB(내부 부하 분산)를 사용하는 개인 IP 주소는 애플리케이션 게이트웨이에 최대 하나의 공용 IP 주소와 하나의 개인 IP 주소를 사용할 수 있습니다.
공용 IP 주소 및 개인 IP 주소는 프런트 엔드 IP 주소로 별도로 추가해야 합니다.

## 예제

### 예제 1: 애플리케이션 게이트웨이의 프런트 엔드 IP로 공용 IP 설정
```
PS C:\>$PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

첫 번째 명령은 공용 IP 주소 개체를 만들고 공용 ip 주소 $PublicIp 저장합니다.
두 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.
세 번째 명령은 $AppGw 저장된 주소를 사용하여 FrontEndIp01이라는 프런트 엔드 IP 구성을 $PublicIp.

### 예제 2: 고정 개인 IP를 애플리케이션 게이트웨이의 프런트 엔드 IP로 설정
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.
두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.
세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.
네 번째 명령은 두 번째 명령의 $Subnet 개인 IP 주소 10.0.1.1을 사용하여 FrontendIP02라는 프런트 엔드 IP 구성을 추가합니다.

### 예제 3: 동적 개인 IP를 애플리케이션 게이트웨이의 프런트 엔드 IP로 설정
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 VNet01이라는 가상 네트워크를 $VNet 변수에 저장합니다.
두 번째 명령은 첫 번째 명령에서 $VNet 사용하여 Subnet01이라는 서브넷 구성을 $Subnet 변수에 저장합니다.
세 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.
네 번째 명령은 두 번째 명령의 명령을 사용하여 FrontendIP02라는 $Subnet IP 구성을 추가합니다.

## PARAMETERS

### -ApplicationGateway
프런트 엔드 IP 구성을 수정할 애플리케이션 게이트웨이 개체를 지정합니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
이 cmdlet이 수정하는 프런트 엔드 IP 구성의 이름을 지정합니다.

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

### -PrivateIPAddress
개인 IP 주소를 지정합니다.
지정된 경우 이 IP는 서브넷에서 정적으로 할당됩니다.

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

### -PrivateLinkConfiguration
PrivateLinkConfiguration

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateLinkConfigurationId
PrivateLinkConfigurationId

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddress
공용 IP 주소를 지정합니다.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIPAddressId
공용 IP 주소의 ID를 지정합니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnet
애플리케이션 게이트웨이에서 사용하는 서브넷을 지정합니다.
게이트웨이가 개인 IP 주소를 사용하는 경우 이 매개 변수를 지정합니다.
*PrivateIPAddress* 주소가 지정된 경우 이 서브넷에 속해야 합니다.
*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
서브넷 ID를 지정합니다.
게이트웨이가 개인 IP 주소를 사용하는 경우 이 매개 변수를 지정합니다.
*PrivateIPAddress* 매개 변수가 지정된 경우 이 서브넷에 속해야 합니다.
*PrivateIPAddress를* 지정하지 않으면 이 서브넷의 IP 주소 중 하나는 애플리케이션 게이트웨이의 프런트 엔드 IP 주소로 동적으로 선택됩니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 참고 사항

## 관련 링크

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Add-AzApplicationGatewayFrontendIPConfig](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Get-AzApplicationGatewayFrontendIPConfig](./Get-AzApplicationGatewayFrontendIPConfig.md)

[New-AzApplicationGatewayFrontendIPConfig](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-AzApplicationGatewayFrontendIPConfig](./Remove-AzApplicationGatewayFrontendIPConfig.md)


