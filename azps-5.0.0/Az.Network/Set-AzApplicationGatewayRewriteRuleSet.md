---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216065"
---
# <span data-ttu-id="7732a-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7732a-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="7732a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7732a-102">SYNOPSIS</span></span>
<span data-ttu-id="7732a-103">응용 프로그램 게이트웨이에 대 한 재작성 규칙 집합을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="7732a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7732a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7732a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7732a-105">DESCRIPTION</span></span>
<span data-ttu-id="7732a-106">**Set-AzApplicationGatewayRewriteRuleSet** cmdlet은 요청 라우팅 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="7732a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7732a-107">EXAMPLES</span></span>

### <span data-ttu-id="7732a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7732a-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="7732a-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7732a-110">두 번째 명령은 $rule 변수에 지정 된 다시 쓰기 규칙을 사용 하도록 응용 프로그램 게이트웨이에 대 한 다시 작성 규칙 집합을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="7732a-111">변수</span><span class="sxs-lookup"><span data-stu-id="7732a-111">PARAMETERS</span></span>

### <span data-ttu-id="7732a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7732a-112">-ApplicationGateway</span></span>
<span data-ttu-id="7732a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7732a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7732a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7732a-114">-DefaultProfile</span></span>
<span data-ttu-id="7732a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7732a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="7732a-116">-Name</span></span>
<span data-ttu-id="7732a-117">RewriteRuleSet의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="7732a-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="7732a-118">-RewriteRule</span></span>
<span data-ttu-id="7732a-119">재작성 규칙 목록</span><span class="sxs-lookup"><span data-stu-id="7732a-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="7732a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7732a-120">CommonParameters</span></span>
<span data-ttu-id="7732a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7732a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7732a-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7732a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7732a-123">입력</span><span class="sxs-lookup"><span data-stu-id="7732a-123">INPUTS</span></span>

### <span data-ttu-id="7732a-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7732a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7732a-125">출력</span><span class="sxs-lookup"><span data-stu-id="7732a-125">OUTPUTS</span></span>

### <span data-ttu-id="7732a-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7732a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7732a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="7732a-127">NOTES</span></span>

## <span data-ttu-id="7732a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7732a-128">RELATED LINKS</span></span>

[<span data-ttu-id="7732a-129">추가-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7732a-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7732a-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7732a-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7732a-131">새로운 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7732a-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7732a-132">제거-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7732a-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7732a-133">새로운 AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7732a-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7732a-134">새로운 AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7732a-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="7732a-135">새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7732a-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)