---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967851"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute 회로 권한 부여에 대한 정보를 얻습니다.

## 구문

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 할당된 권한 부여에 대한 정보를 얻습니다. ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 프레미스 네트워크를 연결합니다. ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다(가상 네트워크당 하나의 권한 부여). 권한 부여 키뿐만 아니라 권한 부여에 대한 기타 정보는 **Get-AzExpressRouteCircuitAuthorization** 을 실행하여 수시로 볼 수 있습니다.

## 예제

### 예제 1: 모든 ExpressRoute 권한 부여를 얻습니다.
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

이러한 명령은 ExpressRoute 회로와 연결된 모든 ExpressRoute 권한 부여에 대한 정보를 반환합니다. 첫 번째 명령은 **Get-AzExpressRouteCircuit** cmdlet을 사용하여 ContosoCircuit라는 회로를 참조하는 개체를 만듭니다. 해당 개체 참조는 변수에 $Circuit. 그런 다음 두 번째 명령은 해당 개체 참조 및 **Get-AzExpressRouteCircuitAuthorization** cmdlet을 사용하여 ContosoCircuit와 연결된 권한 부여에 대한 정보를 반환합니다.

### 예제 2: Where-Object cmdlet을 사용하여 모든 ExpressRoute 권한 부여를 얻습니다.
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

이러한 명령은 예제 1에 사용된 명령의 변형을 나타내고 있습니다. 그러나 이 경우 사용할 수 있는 권한 부여에 대한 정보만 반환됩니다(즉, 가상 네트워크에 할당되지 않은 권한 부여의 경우). 이렇게 하여 회로 권한 부여 정보는 명령 2에서 반환되어 **Where-Object** cmdlet에 파이프됩니다.
**그런 다음 Where-Object는** *AuthorizationUseStatus* 속성이 사용 가능으로 설정된 권한 부여만 선택합니다. 사용할 수 없는 권한 부여만 나열하기 위해 Where 절에 대해 이 구문을 사용하세요. `{$_.AuthorizationUseStatus -ne "Available"}`

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

### -ExpressRouteCircuit
ExpressRoute 회로 권한 부여를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
이 cmdlet이 얻을 ExpressRoute 회로 권한 부여의 이름을 지정합니다.
-Name "ContosoCircuitAuthorization"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## 출력

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## 참고 사항

## 관련 링크

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
