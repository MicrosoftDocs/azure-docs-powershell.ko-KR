---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 5042f7055c9d74dcabc01aa81169c9290816953c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875586"
---
# <span data-ttu-id="b7e86-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7e86-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="b7e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e86-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e86-103">Express 경로 회로에 대 한 라우트 테이블 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b7e86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7e86-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7e86-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b7e86-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e86-106">**AzExpressRouteCircuitRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대 한 BGP 인접 정보 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="b7e86-107">이 정보는 라우팅 컨텍스트가 설정 된 시간과 피어 링 라우터에서 알린 경로 접두사의 수를 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="b7e86-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b7e86-108">EXAMPLES</span></span>

### <span data-ttu-id="b7e86-109">예제 1: 기본 경로의 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="b7e86-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="b7e86-110">변수</span><span class="sxs-lookup"><span data-stu-id="b7e86-110">PARAMETERS</span></span>

### <span data-ttu-id="b7e86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e86-111">-DefaultProfile</span></span>
<span data-ttu-id="b7e86-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7e86-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b7e86-113">-DevicePath</span></span>
<span data-ttu-id="b7e86-114">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b7e86-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e86-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="b7e86-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="b7e86-116">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e86-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b7e86-117">-PeeringType</span></span>
<span data-ttu-id="b7e86-118">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b7e86-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e86-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7e86-120">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e86-121">CommonParameters</span></span>
<span data-ttu-id="b7e86-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e86-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e86-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e86-124">입력</span><span class="sxs-lookup"><span data-stu-id="b7e86-124">INPUTS</span></span>

## <span data-ttu-id="b7e86-125">출력</span><span class="sxs-lookup"><span data-stu-id="b7e86-125">OUTPUTS</span></span>

### <span data-ttu-id="b7e86-126">PSExpressRouteCircuitRoutesTableSummary에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b7e86-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="b7e86-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b7e86-127">NOTES</span></span>

## <span data-ttu-id="b7e86-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7e86-128">RELATED LINKS</span></span>

[<span data-ttu-id="b7e86-129">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b7e86-129">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b7e86-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7e86-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b7e86-131">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="b7e86-131">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)