---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331598"
---
# <span data-ttu-id="fae66-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="fae66-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="fae66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae66-102">SYNOPSIS</span></span>
<span data-ttu-id="fae66-103">새 메트릭 경고를 만드는 데 사용할 수 있는 로컬 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="fae66-104">구문</span><span class="sxs-lookup"><span data-stu-id="fae66-104">SYNTAX</span></span>

### <span data-ttu-id="fae66-105">StaticThresholdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fae66-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae66-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae66-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae66-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae66-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae66-108">설명</span><span class="sxs-lookup"><span data-stu-id="fae66-108">DESCRIPTION</span></span>
<span data-ttu-id="fae66-109">**New-AzMetricAlertRuleV2Criteria** cmdlet은 새 메트릭 경고 규칙을 만드는 [입력 Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet으로 사용할 로컬 메트릭 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="fae66-110">예제</span><span class="sxs-lookup"><span data-stu-id="fae66-110">EXAMPLES</span></span>

### <span data-ttu-id="fae66-111">예제 1: 간단한 메트릭 경고 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="fae66-111">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="fae66-112">이 명령은 메트릭 경고 규칙에 사용할 수 있는 간단한 메트릭 경고 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="fae66-113">예제 2: 동적 메트릭 경고 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="fae66-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="fae66-114">이 명령은 메트릭 경고 규칙에 사용할 수 있는 동적 메트릭 경고 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="fae66-115">예제 3: 더 복잡한 메트릭 경고 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="fae66-115">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="fae66-116">이 명령 집합은 차원 선택을 포함하는 더 복잡한 메트릭 경고 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="fae66-117">예제 4: 웹 사이트 가용성 조건 만들기</span><span class="sxs-lookup"><span data-stu-id="fae66-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="fae66-118">이 명령은 메트릭 경고 규칙에 사용할 수 있는 웹 사이트 가용성 조건을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="fae66-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fae66-119">PARAMETERS</span></span>

### <span data-ttu-id="fae66-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="fae66-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="fae66-121">Application Insights 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae66-122">-DefaultProfile</span></span>
<span data-ttu-id="fae66-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae66-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="fae66-124">-DimensionSelection</span></span>
<span data-ttu-id="fae66-125">차원 조건 목록</span><span class="sxs-lookup"><span data-stu-id="fae66-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="fae66-126">-DynamicThreshold</span></span>
<span data-ttu-id="fae66-127">동적 임계값 형식을 사용하는 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fae66-127">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="fae66-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="fae66-129">검사된 지점의 총 수</span><span class="sxs-lookup"><span data-stu-id="fae66-129">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="fae66-130">-FailedLocationCount</span></span>
<span data-ttu-id="fae66-131">경고를 발생하기 위해 실패한 최소 위치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="fae66-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="fae66-133">IgnoreDataBefore 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fae66-133">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="fae66-134">-MetricName</span></span>
<span data-ttu-id="fae66-135">규칙에 대한 메트릭 이름</span><span class="sxs-lookup"><span data-stu-id="fae66-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="fae66-136">-MetricNamespace</span></span>
<span data-ttu-id="fae66-137">메트릭의 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="fae66-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="fae66-138">-Operator</span></span>
<span data-ttu-id="fae66-139">규칙 조건 연산자</span><span class="sxs-lookup"><span data-stu-id="fae66-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="fae66-140">-SkipMetricValidation</span></span>
<span data-ttu-id="fae66-141">메트릭 유효성 검사를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-142">-Threshold</span><span class="sxs-lookup"><span data-stu-id="fae66-142">-Threshold</span></span>
<span data-ttu-id="fae66-143">규칙 조건에 대한 임계값</span><span class="sxs-lookup"><span data-stu-id="fae66-143">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="fae66-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="fae66-145">규칙 조건에 대한 민감도</span><span class="sxs-lookup"><span data-stu-id="fae66-145">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="fae66-146">-TimeAggregation</span></span>
<span data-ttu-id="fae66-147">기간 간격에 걸쳐 여러 메트릭 값을 롤업하는 데 사용되는 집계 작업</span><span class="sxs-lookup"><span data-stu-id="fae66-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="fae66-148">-ViolationCount</span></span>
<span data-ttu-id="fae66-149">경고를 발생하는 데 필요한 선택한 콜백 기간 내에 필요한 최소 위반 수</span><span class="sxs-lookup"><span data-stu-id="fae66-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="fae66-150">-WebTest</span></span>
<span data-ttu-id="fae66-151">가용성 조건 사용에 대한 매개 변수 전환 형식</span><span class="sxs-lookup"><span data-stu-id="fae66-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="fae66-152">-WebTestId</span></span>
<span data-ttu-id="fae66-153">Application Insights 웹 테스트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae66-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae66-154">CommonParameters</span></span>
<span data-ttu-id="fae66-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fae66-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae66-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fae66-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae66-157">입력</span><span class="sxs-lookup"><span data-stu-id="fae66-157">INPUTS</span></span>

### <span data-ttu-id="fae66-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="fae66-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="fae66-159">출력</span><span class="sxs-lookup"><span data-stu-id="fae66-159">OUTPUTS</span></span>

### <span data-ttu-id="fae66-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="fae66-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="fae66-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fae66-161">NOTES</span></span>

## <span data-ttu-id="fae66-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fae66-162">RELATED LINKS</span></span>