---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 1c59ef12964ddd022add01ae296b8ecac9ad0acd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204044"
---
# <span data-ttu-id="52373-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="52373-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="52373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52373-102">SYNOPSIS</span></span>
<span data-ttu-id="52373-103">Express 경로 회로에서 ARP 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52373-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="52373-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52373-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52373-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52373-105">DESCRIPTION</span></span>
<span data-ttu-id="52373-106">**AzExpressRouteCircuitARPTable** Cmdlet은 express 경로 회로의 두 인터페이스에서 ARP 테이블을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="52373-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="52373-107">ARP 테이블은 특정 피어 링에 대 한 IPv4 주소를 MAC 주소로 매핑하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="52373-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="52373-108">ARP 테이블을 사용 하 여 계층 2 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52373-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="52373-109">예제의</span><span class="sxs-lookup"><span data-stu-id="52373-109">EXAMPLES</span></span>

### <span data-ttu-id="52373-110">예제 1: Express 경로 피어에 대 한 ARP 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="52373-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="52373-111">변수</span><span class="sxs-lookup"><span data-stu-id="52373-111">PARAMETERS</span></span>

### <span data-ttu-id="52373-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52373-112">-DefaultProfile</span></span>
<span data-ttu-id="52373-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52373-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52373-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="52373-114">-DevicePath</span></span>
<span data-ttu-id="52373-115">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="52373-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52373-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="52373-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="52373-117">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52373-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52373-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="52373-118">-PeeringType</span></span>
<span data-ttu-id="52373-119">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="52373-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52373-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52373-120">-ResourceGroupName</span></span>
<span data-ttu-id="52373-121">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52373-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52373-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52373-122">CommonParameters</span></span>
<span data-ttu-id="52373-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52373-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52373-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52373-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52373-125">입력</span><span class="sxs-lookup"><span data-stu-id="52373-125">INPUTS</span></span>

### <span data-ttu-id="52373-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52373-126">System.String</span></span>

## <span data-ttu-id="52373-127">출력</span><span class="sxs-lookup"><span data-stu-id="52373-127">OUTPUTS</span></span>

### <span data-ttu-id="52373-128">PSExpressRouteCircuitArpTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="52373-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="52373-129">상속자</span><span class="sxs-lookup"><span data-stu-id="52373-129">NOTES</span></span>

## <span data-ttu-id="52373-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52373-130">RELATED LINKS</span></span>

[<span data-ttu-id="52373-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="52373-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="52373-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="52373-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="52373-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="52373-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)