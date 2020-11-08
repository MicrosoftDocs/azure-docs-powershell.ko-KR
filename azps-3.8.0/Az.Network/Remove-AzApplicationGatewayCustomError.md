---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042040"
---
# <span data-ttu-id="b4d87-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4d87-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b4d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d87-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d87-103">응용 프로그램 게이트웨이에서 사용자 지정 오류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d87-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="b4d87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4d87-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d87-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4d87-105">DESCRIPTION</span></span>
<span data-ttu-id="b4d87-106">**AzApplicationGatewayCustomError** cmdlet은 응용 프로그램 게이트웨이에서 사용자 지정 오류를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d87-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="b4d87-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b4d87-107">EXAMPLES</span></span>

### <span data-ttu-id="b4d87-108">예제 1: 응용 프로그램 게이트웨이에서 사용자 지정 오류 제거</span><span class="sxs-lookup"><span data-stu-id="b4d87-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="b4d87-109">이 명령은 응용 프로그램 게이트웨이에서 $appgw http 상태 코드 502의 사용자 지정 오류를 제거 하 고 업데이트 된 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d87-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="b4d87-110">변수</span><span class="sxs-lookup"><span data-stu-id="b4d87-110">PARAMETERS</span></span>

### <span data-ttu-id="b4d87-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4d87-111">-ApplicationGateway</span></span>
<span data-ttu-id="b4d87-112">응용 프로그램 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="b4d87-112">The Application Gateway</span></span>

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

### <span data-ttu-id="b4d87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d87-113">-DefaultProfile</span></span>
<span data-ttu-id="b4d87-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d87-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b4d87-115">-StatusCode</span></span>
<span data-ttu-id="b4d87-116">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d87-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b4d87-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d87-117">CommonParameters</span></span>
<span data-ttu-id="b4d87-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d87-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d87-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d87-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d87-120">입력</span><span class="sxs-lookup"><span data-stu-id="b4d87-120">INPUTS</span></span>

### <span data-ttu-id="b4d87-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4d87-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4d87-122">출력</span><span class="sxs-lookup"><span data-stu-id="b4d87-122">OUTPUTS</span></span>

### <span data-ttu-id="b4d87-123">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4d87-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b4d87-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b4d87-124">NOTES</span></span>

## <span data-ttu-id="b4d87-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4d87-125">RELATED LINKS</span></span>

[<span data-ttu-id="b4d87-126">추가-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4d87-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b4d87-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4d87-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b4d87-128">새로운 AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4d87-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b4d87-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b4d87-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)