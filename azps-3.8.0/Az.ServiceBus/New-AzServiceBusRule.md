---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034772"
---
# <span data-ttu-id="3f623-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="3f623-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="3f623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f623-102">SYNOPSIS</span></span>
<span data-ttu-id="3f623-103">항목의 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="3f623-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f623-104">SYNTAX</span></span>

### <span data-ttu-id="3f623-105">Rule속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f623-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f623-106">Ruleaction속성 집합</span><span class="sxs-lookup"><span data-stu-id="3f623-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f623-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3f623-107">DESCRIPTION</span></span>
<span data-ttu-id="3f623-108">**AzServiceBusRule** cmdlet은 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="3f623-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3f623-109">EXAMPLES</span></span>

### <span data-ttu-id="3f623-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f623-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="3f623-111">New-AzServiceBusRule cmdlet은 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="3f623-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="3f623-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="3f623-113">New-AzServiceBusRule cmdlet은 ActionFilter를 사용 하 여 지정 된 구독에 대 한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="3f623-114">변수</span><span class="sxs-lookup"><span data-stu-id="3f623-114">PARAMETERS</span></span>

### <span data-ttu-id="3f623-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="3f623-115">-ActionSqlExpression</span></span>
<span data-ttu-id="3f623-116">Action SqlFilter 식</span><span class="sxs-lookup"><span data-stu-id="3f623-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f623-117">-DefaultProfile</span></span>
<span data-ttu-id="3f623-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f623-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3f623-119">-Name</span></span>
<span data-ttu-id="3f623-120">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="3f623-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3f623-121">-Namespace</span></span>
<span data-ttu-id="3f623-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3f623-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="3f623-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="3f623-124">작업 전처리 필요</span><span class="sxs-lookup"><span data-stu-id="3f623-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f623-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f623-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-126">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="3f623-127">-SqlExpression</span></span>
<span data-ttu-id="3f623-128">Sql 필터 식</span><span class="sxs-lookup"><span data-stu-id="3f623-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-129">-구독</span><span class="sxs-lookup"><span data-stu-id="3f623-129">-Subscription</span></span>
<span data-ttu-id="3f623-130">구독 이름</span><span class="sxs-lookup"><span data-stu-id="3f623-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-131">-주제</span><span class="sxs-lookup"><span data-stu-id="3f623-131">-Topic</span></span>
<span data-ttu-id="3f623-132">주제 이름</span><span class="sxs-lookup"><span data-stu-id="3f623-132">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-133">-확인</span><span class="sxs-lookup"><span data-stu-id="3f623-133">-Confirm</span></span>
<span data-ttu-id="3f623-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f623-135">-WhatIf</span></span>
<span data-ttu-id="3f623-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f623-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f623-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f623-138">CommonParameters</span></span>
<span data-ttu-id="3f623-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f623-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f623-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f623-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f623-141">입력</span><span class="sxs-lookup"><span data-stu-id="3f623-141">INPUTS</span></span>

### <span data-ttu-id="3f623-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3f623-142">System.String</span></span>

## <span data-ttu-id="3f623-143">출력</span><span class="sxs-lookup"><span data-stu-id="3f623-143">OUTPUTS</span></span>

### <span data-ttu-id="3f623-144">ServiceBus. Ps규칙 특성을</span><span class="sxs-lookup"><span data-stu-id="3f623-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3f623-145">상속자</span><span class="sxs-lookup"><span data-stu-id="3f623-145">NOTES</span></span>

## <span data-ttu-id="3f623-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f623-146">RELATED LINKS</span></span>