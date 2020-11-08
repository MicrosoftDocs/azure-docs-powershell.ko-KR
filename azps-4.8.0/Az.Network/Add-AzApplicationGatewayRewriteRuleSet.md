---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048955"
---
# <span data-ttu-id="59fc4-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59fc4-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="59fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="59fc4-103">응용 프로그램 게이트웨이에 다시 쓰기 규칙 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="59fc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59fc4-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fc4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="59fc4-106">**AzApplicationGatewayRewriteRuleSet** cmdlet은 응용 프로그램 게이트웨이에 다시 작성 규칙 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="59fc4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="59fc4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="59fc4-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="59fc4-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="59fc4-110">두 번째 명령은 응용 프로그램 게이트웨이에 다시 작성 규칙 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="59fc4-111">변수</span><span class="sxs-lookup"><span data-stu-id="59fc4-111">PARAMETERS</span></span>

### <span data-ttu-id="59fc4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59fc4-112">-ApplicationGateway</span></span>
<span data-ttu-id="59fc4-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59fc4-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59fc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fc4-114">-DefaultProfile</span></span>
<span data-ttu-id="59fc4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59fc4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="59fc4-116">-Name</span></span>
<span data-ttu-id="59fc4-117">RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="59fc4-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="59fc4-118">-RewriteRule</span></span>
<span data-ttu-id="59fc4-119">재작성 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="59fc4-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fc4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fc4-120">CommonParameters</span></span>
<span data-ttu-id="59fc4-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fc4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fc4-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fc4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fc4-123">입력</span><span class="sxs-lookup"><span data-stu-id="59fc4-123">INPUTS</span></span>

### <span data-ttu-id="59fc4-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59fc4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59fc4-125">출력</span><span class="sxs-lookup"><span data-stu-id="59fc4-125">OUTPUTS</span></span>

### <span data-ttu-id="59fc4-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59fc4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59fc4-127">상속자</span><span class="sxs-lookup"><span data-stu-id="59fc4-127">NOTES</span></span>

## <span data-ttu-id="59fc4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59fc4-128">RELATED LINKS</span></span>

[<span data-ttu-id="59fc4-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59fc4-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59fc4-130">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59fc4-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59fc4-131">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59fc4-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59fc4-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="59fc4-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="59fc4-133">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="59fc4-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="59fc4-134">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="59fc4-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="59fc4-135">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="59fc4-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)