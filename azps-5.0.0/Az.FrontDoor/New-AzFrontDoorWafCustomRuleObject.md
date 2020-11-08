---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217409"
---
# <span data-ttu-id="3e6f4-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="3e6f4-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="3e6f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6f4-103">WAF 정책 만들기에 대 한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3e6f4-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="3e6f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e6f4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e6f4-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6f4-106">WAF 정책 만들기에 대 한 CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3e6f4-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="3e6f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3e6f4-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6f4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e6f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="3e6f4-109">CustomRule 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3e6f4-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="3e6f4-110">변수</span><span class="sxs-lookup"><span data-stu-id="3e6f4-110">PARAMETERS</span></span>

### <span data-ttu-id="3e6f4-111">-작업</span><span class="sxs-lookup"><span data-stu-id="3e6f4-111">-Action</span></span>
<span data-ttu-id="3e6f4-112">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-112">Type of Actions.</span></span>
<span data-ttu-id="3e6f4-113">사용할 수 있는 값은 다음과 같습니다. ' 허용 ', ' 차단 ', ' 로그 '</span><span class="sxs-lookup"><span data-stu-id="3e6f4-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="3e6f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6f4-114">-DefaultProfile</span></span>
<span data-ttu-id="3e6f4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6f4-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="3e6f4-116">-EnabledState</span></span>
<span data-ttu-id="3e6f4-117">사용할 수 있는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-117">Enabled State.</span></span> <span data-ttu-id="3e6f4-118">가능한 값은 ' Enabled ', ' Disabled '입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="3e6f4-119">MatchCondition</span><span class="sxs-lookup"><span data-stu-id="3e6f4-119">-MatchCondition</span></span>
<span data-ttu-id="3e6f4-120">일치 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-120">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3e6f4-121">-Name</span></span>
<span data-ttu-id="3e6f4-122">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="3e6f4-122">Name of the rule</span></span>

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

### <span data-ttu-id="3e6f4-123">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="3e6f4-123">-Priority</span></span>
<span data-ttu-id="3e6f4-124">규칙의 우선 순위를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-124">Describes priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f4-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="3e6f4-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="3e6f4-126">속도 제한 기간</span><span class="sxs-lookup"><span data-stu-id="3e6f4-126">Rate limit duration.</span></span> <span data-ttu-id="3e6f4-127">기본값-1 분</span><span class="sxs-lookup"><span data-stu-id="3e6f4-127">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f4-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="3e6f4-128">-RateLimitThreshold</span></span>
<span data-ttu-id="3e6f4-129">속도 제한 임계값</span><span class="sxs-lookup"><span data-stu-id="3e6f4-129">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f4-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="3e6f4-130">-RuleType</span></span>
<span data-ttu-id="3e6f4-131">규칙의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-131">Type of the rule.</span></span>
<span data-ttu-id="3e6f4-132">사용할 수 있는 값은 다음과 같습니다. ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="3e6f4-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="3e6f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6f4-133">CommonParameters</span></span>
<span data-ttu-id="3e6f4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6f4-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6f4-136">입력</span><span class="sxs-lookup"><span data-stu-id="3e6f4-136">INPUTS</span></span>

### <span data-ttu-id="3e6f4-137">않아야</span><span class="sxs-lookup"><span data-stu-id="3e6f4-137">None</span></span>

## <span data-ttu-id="3e6f4-138">출력</span><span class="sxs-lookup"><span data-stu-id="3e6f4-138">OUTPUTS</span></span>

### <span data-ttu-id="3e6f4-139">FrontDoor. PSCustomRule/.</span><span class="sxs-lookup"><span data-stu-id="3e6f4-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="3e6f4-140">상속자</span><span class="sxs-lookup"><span data-stu-id="3e6f4-140">NOTES</span></span>

## <span data-ttu-id="3e6f4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e6f4-141">RELATED LINKS</span></span>

<span data-ttu-id="3e6f4-142">[새로운 AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [업데이트-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3e6f4-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>