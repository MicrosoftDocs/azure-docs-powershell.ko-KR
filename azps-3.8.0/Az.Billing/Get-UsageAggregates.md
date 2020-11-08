---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042404"
---
# <span data-ttu-id="0dee5-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="0dee5-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="0dee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dee5-102">SYNOPSIS</span></span>
<span data-ttu-id="0dee5-103">보고 된 Azure 구독 사용량 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="0dee5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0dee5-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dee5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0dee5-105">DESCRIPTION</span></span>
<span data-ttu-id="0dee5-106">**UsageAggregates** cmdlet은 다음 속성으로 집계 된 Azure 구독 사용 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="0dee5-107">사용이 보고 된 시작 시간과 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="0dee5-108">집계 정밀도 (매일 또는 매시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="0dee5-109">동일한 리소스의 여러 인스턴스에 대 한 인스턴스 수준 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="0dee5-110">일관적인 결과를 위해, 반환 되는 데이터는 Azure 리소스에서 사용 현황 세부 정보를 보고 한 시기를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="0dee5-111">자세한 내용은 https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Microsoft 개발자 네트워크 라이브러리의 AZURE 청구 REST API 참조를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0dee5-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="0dee5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0dee5-112">EXAMPLES</span></span>

### <span data-ttu-id="0dee5-113">예제 1: 구독 데이터 검색</span><span class="sxs-lookup"><span data-stu-id="0dee5-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="0dee5-114">이 명령은 5/2/2015와 5/5/2015 사이의 구독에 대 한 보고 된 사용량 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="0dee5-115">변수</span><span class="sxs-lookup"><span data-stu-id="0dee5-115">PARAMETERS</span></span>

### <span data-ttu-id="0dee5-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="0dee5-116">-AggregationGranularity</span></span>
<span data-ttu-id="0dee5-117">데이터의 집계 정밀도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="0dee5-118">유효한 값은 일일 및 매시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="0dee5-119">기본값은 일일 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee5-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="0dee5-120">-ContinuationToken</span></span>
<span data-ttu-id="0dee5-121">이전 호출의 응답 본문에서 검색 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="0dee5-122">큰 결과 집합의 경우 연속 토큰을 사용 하 여 응답을 페이징할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="0dee5-123">연속 토큰은 진행률에 대 한 책갈피 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="0dee5-124">이 매개 변수를 지정 하지 않으면 데이터는 *ReportedStartTime* 에 지정 된 일 또는 시간의 시작 부분에서 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="0dee5-125">응답에서 다음 링크를 통해 데이터 페이지를 참조 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="0dee5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dee5-126">-DefaultProfile</span></span>
<span data-ttu-id="0dee5-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dee5-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="0dee5-128">-ReportedEndTime</span></span>
<span data-ttu-id="0dee5-129">Azure 청구 시스템에 리소스 사용이 기록 된 시점에 대해 보고 된 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="0dee5-130">Azure는 전세계 여러 데이터 센터에 걸친 분산 시스템 이므로 리소스가 실제로 소모 된 시기 (리소스 사용 시간)와 사용 이벤트가 청구 시스템에 도달 했을 때 리소스 사용이 보고 된 시간 사이에는 지연이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="0dee5-131">특정 기간 동안 보고 되는 구독에 대 한 모든 사용 이벤트를 가져오려면 보고 된 시간을 쿼리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="0dee5-132">보고 된 시간을 기준으로 쿼리 하는 경우에도 cmdlet은 리소스 사용 시간을 기준으로 응답 데이터를 집계 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="0dee5-133">리소스 사용 데이터는 데이터 분석에 유용한 피벗입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee5-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="0dee5-134">-ReportedStartTime</span></span>
<span data-ttu-id="0dee5-135">Azure 청구 시스템에서 리소스 사용이 기록 된 시점에 대해 보고 된 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee5-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="0dee5-136">-ShowDetails</span></span>
<span data-ttu-id="0dee5-137">이 cmdlet이 사용 데이터와 함께 인스턴스 수준의 세부 정보를 반환 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="0dee5-138">기본값은 $True입니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-138">The default value is $True.</span></span>
<span data-ttu-id="0dee5-139">$False 경우 서비스는 서버 쪽에서 결과를 집계 하므로 집계 그룹을 더 적게 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="0dee5-140">예를 들어 세 개의 웹 사이트를 실행 하는 경우 기본적으로 웹 사이트를 사용 하는 세 개의 회선 항목이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="0dee5-141">그러나 값이 $False 되 면 동일한 **subscriptionId** , **meterId** , **usageStartTime** 및 **usageEndTime** 에 대 한 모든 데이터가 단일 줄 항목으로 축소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dee5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dee5-142">CommonParameters</span></span>
<span data-ttu-id="0dee5-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dee5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dee5-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dee5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dee5-145">입력</span><span class="sxs-lookup"><span data-stu-id="0dee5-145">INPUTS</span></span>

### <span data-ttu-id="0dee5-146">않아야</span><span class="sxs-lookup"><span data-stu-id="0dee5-146">None</span></span>

## <span data-ttu-id="0dee5-147">출력</span><span class="sxs-lookup"><span data-stu-id="0dee5-147">OUTPUTS</span></span>

### <span data-ttu-id="0dee5-148">Microsoft UsageAggregates. UsageAggregationGetResponse.</span><span class="sxs-lookup"><span data-stu-id="0dee5-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="0dee5-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0dee5-149">NOTES</span></span>

## <span data-ttu-id="0dee5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0dee5-150">RELATED LINKS</span></span>