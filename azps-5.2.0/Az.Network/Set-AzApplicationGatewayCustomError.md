---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370938"
---
# <span data-ttu-id="9df2a-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9df2a-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9df2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df2a-102">SYNOPSIS</span></span>
<span data-ttu-id="9df2a-103">애플리케이션 게이트웨이에서 사용자 지정 오류를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="9df2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9df2a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9df2a-105">설명</span><span class="sxs-lookup"><span data-stu-id="9df2a-105">DESCRIPTION</span></span>
<span data-ttu-id="9df2a-106">**Set-AzApplicationGatewayCustomError** cmdlet은 애플리케이션 게이트웨이에서 사용자 지정 오류를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="9df2a-107">예제</span><span class="sxs-lookup"><span data-stu-id="9df2a-107">EXAMPLES</span></span>

### <span data-ttu-id="9df2a-108">예제 1: 애플리케이션 게이트웨이에서 사용자 지정 오류 업데이트</span><span class="sxs-lookup"><span data-stu-id="9df2a-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="9df2a-109">이 명령은 애플리케이션 게이트웨이에서 http 상태 코드 502의 사용자 지정 오류를 $appgw 업데이트된 게이트웨이를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="9df2a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9df2a-110">PARAMETERS</span></span>

### <span data-ttu-id="9df2a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9df2a-111">-ApplicationGateway</span></span>
<span data-ttu-id="9df2a-112">The Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9df2a-112">The Application Gateway</span></span>

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

### <span data-ttu-id="9df2a-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="9df2a-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="9df2a-114">애플리케이션 게이트웨이 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9df2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df2a-115">-DefaultProfile</span></span>
<span data-ttu-id="9df2a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9df2a-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9df2a-117">-StatusCode</span></span>
<span data-ttu-id="9df2a-118">애플리케이션 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9df2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df2a-119">CommonParameters</span></span>
<span data-ttu-id="9df2a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9df2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df2a-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9df2a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df2a-122">입력</span><span class="sxs-lookup"><span data-stu-id="9df2a-122">INPUTS</span></span>

### <span data-ttu-id="9df2a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9df2a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9df2a-124">출력</span><span class="sxs-lookup"><span data-stu-id="9df2a-124">OUTPUTS</span></span>

### <span data-ttu-id="9df2a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9df2a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9df2a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9df2a-126">NOTES</span></span>

## <span data-ttu-id="9df2a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9df2a-127">RELATED LINKS</span></span>

[<span data-ttu-id="9df2a-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9df2a-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9df2a-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9df2a-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9df2a-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9df2a-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9df2a-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9df2a-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)