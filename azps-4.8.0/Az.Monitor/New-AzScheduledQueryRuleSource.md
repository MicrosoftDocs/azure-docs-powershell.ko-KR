---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 931b1b39a61b1e2c879b8be1723c5ce9e90638a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214419"
---
# <span data-ttu-id="f063a-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f063a-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="f063a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f063a-102">SYNOPSIS</span></span>
<span data-ttu-id="f063a-103">원본 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-103">Creates an object of type Source</span></span>

## <span data-ttu-id="f063a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f063a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f063a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f063a-105">DESCRIPTION</span></span>
<span data-ttu-id="f063a-106">Source 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-106">Creates an object of type Source.</span></span>
<span data-ttu-id="f063a-107">이 개체는 로그 알림 규칙을 만드는 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="f063a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f063a-108">EXAMPLES</span></span>

### <span data-ttu-id="f063a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f063a-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

### <span data-ttu-id="f063a-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="f063a-110">Example 2</span></span>

<span data-ttu-id="f063a-111">Source 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-111">Creates an object of type Source.</span></span> <span data-ttu-id="f063a-112">생성</span><span class="sxs-lookup"><span data-stu-id="f063a-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzScheduledQueryRuleSource -DataSourceId <String> -Query 'Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)'
```

## <span data-ttu-id="f063a-113">변수</span><span class="sxs-lookup"><span data-stu-id="f063a-113">PARAMETERS</span></span>

### <span data-ttu-id="f063a-114">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="f063a-114">-AuthorizedResource</span></span>
<span data-ttu-id="f063a-115">이 경고에 대 한 승인 된 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="f063a-115">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f063a-116">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="f063a-116">-DataSourceId</span></span>
<span data-ttu-id="f063a-117">이 경고가 생성 되는 데이터 원본</span><span class="sxs-lookup"><span data-stu-id="f063a-117">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="f063a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f063a-118">-DefaultProfile</span></span>
<span data-ttu-id="f063a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f063a-120">-쿼리</span><span class="sxs-lookup"><span data-stu-id="f063a-120">-Query</span></span>
<span data-ttu-id="f063a-121">알림 쿼리</span><span class="sxs-lookup"><span data-stu-id="f063a-121">The alert query</span></span>

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

### <span data-ttu-id="f063a-122">-QueryType</span><span class="sxs-lookup"><span data-stu-id="f063a-122">-QueryType</span></span>
<span data-ttu-id="f063a-123">쿼리 형식-현재 지원 되는 값: ResultCount</span><span class="sxs-lookup"><span data-stu-id="f063a-123">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="f063a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f063a-124">CommonParameters</span></span>
<span data-ttu-id="f063a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f063a-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f063a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f063a-127">입력</span><span class="sxs-lookup"><span data-stu-id="f063a-127">INPUTS</span></span>

### <span data-ttu-id="f063a-128">않아야</span><span class="sxs-lookup"><span data-stu-id="f063a-128">None</span></span>

## <span data-ttu-id="f063a-129">출력</span><span class="sxs-lookup"><span data-stu-id="f063a-129">OUTPUTS</span></span>

### <span data-ttu-id="f063a-130">PSScheduledQueryRuleSource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f063a-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="f063a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f063a-131">NOTES</span></span>

## <span data-ttu-id="f063a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f063a-132">RELATED LINKS</span></span>