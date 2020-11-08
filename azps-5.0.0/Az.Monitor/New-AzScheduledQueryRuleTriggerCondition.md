---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226639"
---
# <span data-ttu-id="8b45f-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8b45f-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="8b45f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b45f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b45f-103">트리거 조건 유형의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="8b45f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b45f-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b45f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b45f-105">DESCRIPTION</span></span>
<span data-ttu-id="8b45f-106">트리거 조건 유형의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="8b45f-107">이 개체는 경고 동작 개체를 만드는 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="8b45f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8b45f-108">EXAMPLES</span></span>

### <span data-ttu-id="8b45f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b45f-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="8b45f-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b45f-110">PARAMETERS</span></span>

### <span data-ttu-id="8b45f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b45f-111">-DefaultProfile</span></span>
<span data-ttu-id="8b45f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b45f-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8b45f-113">-MetricTrigger</span></span>
<span data-ttu-id="8b45f-114">메트릭 쿼리 규칙에 대 한 트리거 조건</span><span class="sxs-lookup"><span data-stu-id="8b45f-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b45f-115">-임계값</span><span class="sxs-lookup"><span data-stu-id="8b45f-115">-Threshold</span></span>
<span data-ttu-id="8b45f-116">경고가 발생 하는 임계값입니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-116">The threshold above which alert gets fired</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b45f-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="8b45f-117">-ThresholdOperator</span></span>
<span data-ttu-id="8b45f-118">임계값 연산자: GreaterThan, LessThan 또는 같음</span><span class="sxs-lookup"><span data-stu-id="8b45f-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="8b45f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b45f-119">CommonParameters</span></span>
<span data-ttu-id="8b45f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b45f-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b45f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b45f-122">입력</span><span class="sxs-lookup"><span data-stu-id="8b45f-122">INPUTS</span></span>

### <span data-ttu-id="8b45f-123">않아야</span><span class="sxs-lookup"><span data-stu-id="8b45f-123">None</span></span>

## <span data-ttu-id="8b45f-124">출력</span><span class="sxs-lookup"><span data-stu-id="8b45f-124">OUTPUTS</span></span>

### <span data-ttu-id="8b45f-125">PSScheduledQueryRuleTriggerCondition를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b45f-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="8b45f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8b45f-126">NOTES</span></span>

## <span data-ttu-id="8b45f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b45f-127">RELATED LINKS</span></span>