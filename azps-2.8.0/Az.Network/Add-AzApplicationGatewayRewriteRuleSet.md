---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 4b2b8f2694377845af92db5809230a423f83d594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870893"
---
# <span data-ttu-id="cc6f2-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="cc6f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6f2-103">응용 프로그램 게이트웨이에 다시 쓰기 규칙 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="cc6f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc6f2-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc6f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc6f2-105">DESCRIPTION</span></span>
<span data-ttu-id="cc6f2-106">**AzApplicationGatewayRewriteRuleSet** cmdlet은 응용 프로그램 게이트웨이에 다시 작성 규칙 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="cc6f2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc6f2-107">EXAMPLES</span></span>

### <span data-ttu-id="cc6f2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc6f2-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="cc6f2-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cc6f2-110">두 번째 명령은 응용 프로그램 게이트웨이에 다시 작성 규칙 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="cc6f2-111">변수</span><span class="sxs-lookup"><span data-stu-id="cc6f2-111">PARAMETERS</span></span>

### <span data-ttu-id="cc6f2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6f2-112">-ApplicationGateway</span></span>
<span data-ttu-id="cc6f2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6f2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cc6f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6f2-114">-DefaultProfile</span></span>
<span data-ttu-id="cc6f2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc6f2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="cc6f2-116">-Name</span></span>
<span data-ttu-id="cc6f2-117">RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="cc6f2-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="cc6f2-118">-RewriteRule</span></span>
<span data-ttu-id="cc6f2-119">재작성 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="cc6f2-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="cc6f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6f2-120">CommonParameters</span></span>
<span data-ttu-id="cc6f2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6f2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc6f2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6f2-123">입력</span><span class="sxs-lookup"><span data-stu-id="cc6f2-123">INPUTS</span></span>

### <span data-ttu-id="cc6f2-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6f2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc6f2-125">출력</span><span class="sxs-lookup"><span data-stu-id="cc6f2-125">OUTPUTS</span></span>

### <span data-ttu-id="cc6f2-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc6f2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc6f2-127">상속자</span><span class="sxs-lookup"><span data-stu-id="cc6f2-127">NOTES</span></span>

## <span data-ttu-id="cc6f2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc6f2-128">RELATED LINKS</span></span>

[<span data-ttu-id="cc6f2-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cc6f2-130">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cc6f2-131">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cc6f2-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="cc6f2-133">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cc6f2-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="cc6f2-134">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="cc6f2-135">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc6f2-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)