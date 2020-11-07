---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 5eab973f7a5c5f6221d4c02d94702a4d4a549204
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875772"
---
# <span data-ttu-id="6fbce-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="6fbce-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="6fbce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbce-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbce-103">메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-103">Gets metric definitions.</span></span>

## <span data-ttu-id="6fbce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6fbce-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fbce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6fbce-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbce-106">**Get-AzMetricDefinition** cmdlet은 메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="6fbce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6fbce-107">EXAMPLES</span></span>

### <span data-ttu-id="6fbce-108">예제 1: 리소스에 대 한 메트릭 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="6fbce-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="6fbce-109">이 명령은 지정 된 리소스에 대 한 메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="6fbce-110">예제 2: 자세한 출력을 사용 하 여 메트릭 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="6fbce-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="6fbce-111">이 명령은 website2에 대 한 메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="6fbce-112">출력이 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-112">The output is detailed.</span></span>

### <span data-ttu-id="6fbce-113">예제 3: 이름별 메트릭 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="6fbce-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="6fbce-114">이 명령은 BytesSent 및 CpuTime 메트릭스에 대 한 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="6fbce-115">출력이 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-115">The output is detailed.</span></span>

## <span data-ttu-id="6fbce-116">변수</span><span class="sxs-lookup"><span data-stu-id="6fbce-116">PARAMETERS</span></span>

### <span data-ttu-id="6fbce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbce-117">-DefaultProfile</span></span>
<span data-ttu-id="6fbce-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6fbce-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fbce-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="6fbce-119">-DetailedOutput</span></span>
<span data-ttu-id="6fbce-120">이 작업에 자세한 출력이 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="6fbce-121">이 매개 변수를 지정 하지 않으면 출력이 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="6fbce-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="6fbce-122">-MetricName</span></span>
<span data-ttu-id="6fbce-123">메트릭의 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbce-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="6fbce-124">-MetricNamespace</span></span>
<span data-ttu-id="6fbce-125">메트릭 정의를 쿼리할 메트릭 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="6fbce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fbce-126">-ResourceId</span></span>
<span data-ttu-id="6fbce-127">리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-127">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbce-128">CommonParameters</span></span>
<span data-ttu-id="6fbce-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbce-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6fbce-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbce-131">입력</span><span class="sxs-lookup"><span data-stu-id="6fbce-131">INPUTS</span></span>

### <span data-ttu-id="6fbce-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6fbce-132">System.String</span></span>

### <span data-ttu-id="6fbce-133">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="6fbce-133">System.String[]</span></span>

## <span data-ttu-id="6fbce-134">출력</span><span class="sxs-lookup"><span data-stu-id="6fbce-134">OUTPUTS</span></span>

### <span data-ttu-id="6fbce-135">PSMetricDefinition를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6fbce-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="6fbce-136">상속자</span><span class="sxs-lookup"><span data-stu-id="6fbce-136">NOTES</span></span>

<span data-ttu-id="6fbce-137">지원 되는 메트릭에 대 한 자세한 내용은 다음에서 찾을 수 있습니다. https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="6fbce-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="6fbce-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fbce-138">RELATED LINKS</span></span>

<span data-ttu-id="6fbce-139">[Get-AzMetric](./Get-AzMetric.md) 
 [새로운 AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="6fbce-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>

