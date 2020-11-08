---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046992"
---
# <span data-ttu-id="3616c-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="3616c-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="3616c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3616c-102">SYNOPSIS</span></span>
<span data-ttu-id="3616c-103">지정 된 계획의 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="3616c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3616c-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3616c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3616c-105">DESCRIPTION</span></span>
<span data-ttu-id="3616c-106">지정 된 계획의 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="3616c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3616c-107">EXAMPLES</span></span>

### <span data-ttu-id="3616c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3616c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="3616c-109">계획의 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="3616c-110">변수</span><span class="sxs-lookup"><span data-stu-id="3616c-110">PARAMETERS</span></span>

### <span data-ttu-id="3616c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3616c-111">-DefaultProfile</span></span>
<span data-ttu-id="3616c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3616c-113">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="3616c-113">-PlanName</span></span>
<span data-ttu-id="3616c-114">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-114">Name of the plan.</span></span>

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

### <span data-ttu-id="3616c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3616c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3616c-116">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3616c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3616c-117">-SubscriptionId</span></span>
<span data-ttu-id="3616c-118">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3616c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3616c-119">CommonParameters</span></span>
<span data-ttu-id="3616c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3616c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3616c-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3616c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3616c-122">입력</span><span class="sxs-lookup"><span data-stu-id="3616c-122">INPUTS</span></span>

## <span data-ttu-id="3616c-123">출력</span><span class="sxs-lookup"><span data-stu-id="3616c-123">OUTPUTS</span></span>

### <span data-ttu-id="3616c-124">SubscriptionsAdmin. Api20151101. IMetricList에 대 한</span><span class="sxs-lookup"><span data-stu-id="3616c-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="3616c-125">별칭과</span><span class="sxs-lookup"><span data-stu-id="3616c-125">ALIASES</span></span>

## <span data-ttu-id="3616c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3616c-126">NOTES</span></span>

## <span data-ttu-id="3616c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3616c-127">RELATED LINKS</span></span>
