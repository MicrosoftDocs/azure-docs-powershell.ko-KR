---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056196"
---
# <span data-ttu-id="77c46-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="77c46-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="77c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77c46-102">SYNOPSIS</span></span>
<span data-ttu-id="77c46-103">Application gateway에 대 한 재작성 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77c46-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="77c46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77c46-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77c46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="77c46-105">DESCRIPTION</span></span>
<span data-ttu-id="77c46-106">**AzApplicationGatewayRewriteRule Cmdlet은** Azure application gateway에 대 한 재작성 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77c46-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="77c46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="77c46-107">EXAMPLES</span></span>

### <span data-ttu-id="77c46-108">예제 1: 응용 프로그램 게이트웨이에 대 한 다시 작성 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="77c46-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="77c46-109">이 명령은 rule1 이라는 재작성 규칙을 만들고 그 결과를 $rule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c46-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="77c46-110">변수</span><span class="sxs-lookup"><span data-stu-id="77c46-110">PARAMETERS</span></span>

### <span data-ttu-id="77c46-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="77c46-111">-ActionSet</span></span>
<span data-ttu-id="77c46-112">다시 쓰기 규칙의 ActionSet</span><span class="sxs-lookup"><span data-stu-id="77c46-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c46-113">-조건</span><span class="sxs-lookup"><span data-stu-id="77c46-113">-Condition</span></span>
<span data-ttu-id="77c46-114">재작성 규칙이 실행 되는 조건</span><span class="sxs-lookup"><span data-stu-id="77c46-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c46-115">-DefaultProfile</span></span>
<span data-ttu-id="77c46-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77c46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77c46-117">-이름</span><span class="sxs-lookup"><span data-stu-id="77c46-117">-Name</span></span>
<span data-ttu-id="77c46-118">RewriteRule의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77c46-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="77c46-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="77c46-119">-RuleSequence</span></span>
<span data-ttu-id="77c46-120">다시 작성 규칙 집합에서이 재작성 규칙의 규칙 순서 지정</span><span class="sxs-lookup"><span data-stu-id="77c46-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="77c46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c46-121">CommonParameters</span></span>
<span data-ttu-id="77c46-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c46-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c46-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c46-124">입력</span><span class="sxs-lookup"><span data-stu-id="77c46-124">INPUTS</span></span>

### <span data-ttu-id="77c46-125">않아야</span><span class="sxs-lookup"><span data-stu-id="77c46-125">None</span></span>

## <span data-ttu-id="77c46-126">출력</span><span class="sxs-lookup"><span data-stu-id="77c46-126">OUTPUTS</span></span>

### <span data-ttu-id="77c46-127">PSApplicationGatewayRewriteRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="77c46-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="77c46-128">상속자</span><span class="sxs-lookup"><span data-stu-id="77c46-128">NOTES</span></span>

## <span data-ttu-id="77c46-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77c46-129">RELATED LINKS</span></span>

[<span data-ttu-id="77c46-130">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="77c46-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="77c46-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="77c46-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="77c46-132">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="77c46-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="77c46-133">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="77c46-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="77c46-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="77c46-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="77c46-135">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="77c46-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="77c46-136">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="77c46-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)