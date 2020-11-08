---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204566"
---
# <span data-ttu-id="a5cd2-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a5cd2-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="a5cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a5cd2-103">Express 경로 회로에 대 한 라우트 테이블 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a5cd2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5cd2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5cd2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a5cd2-106">**AzExpressRouteCircuitRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대 한 BGP 인접 정보 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="a5cd2-107">이 정보는 라우팅 컨텍스트가 설정 된 시간과 피어 링 라우터에서 알린 경로 접두사의 수를 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="a5cd2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a5cd2-108">EXAMPLES</span></span>

### <span data-ttu-id="a5cd2-109">예제 1: 기본 경로의 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="a5cd2-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="a5cd2-110">변수</span><span class="sxs-lookup"><span data-stu-id="a5cd2-110">PARAMETERS</span></span>

### <span data-ttu-id="a5cd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5cd2-111">-DefaultProfile</span></span>
<span data-ttu-id="a5cd2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5cd2-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="a5cd2-113">-DevicePath</span></span>
<span data-ttu-id="a5cd2-114">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="a5cd2-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="a5cd2-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="a5cd2-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="a5cd2-116">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="a5cd2-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="a5cd2-117">-PeeringType</span></span>
<span data-ttu-id="a5cd2-118">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="a5cd2-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="a5cd2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5cd2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5cd2-120">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="a5cd2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5cd2-121">CommonParameters</span></span>
<span data-ttu-id="a5cd2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5cd2-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5cd2-124">입력</span><span class="sxs-lookup"><span data-stu-id="a5cd2-124">INPUTS</span></span>

### <span data-ttu-id="a5cd2-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5cd2-125">System.String</span></span>

## <span data-ttu-id="a5cd2-126">출력</span><span class="sxs-lookup"><span data-stu-id="a5cd2-126">OUTPUTS</span></span>

### <span data-ttu-id="a5cd2-127">PSExpressRouteCircuitRoutesTableSummary에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a5cd2-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="a5cd2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="a5cd2-128">NOTES</span></span>

## <span data-ttu-id="a5cd2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5cd2-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5cd2-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a5cd2-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="a5cd2-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a5cd2-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="a5cd2-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="a5cd2-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)