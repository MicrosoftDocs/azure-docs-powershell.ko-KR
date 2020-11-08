---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047722"
---
# <span data-ttu-id="b335c-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b335c-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="b335c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b335c-102">SYNOPSIS</span></span>
<span data-ttu-id="b335c-103">사용자 지정 오류를 응용 프로그램 게이트웨이의 http 수신기에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="b335c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b335c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b335c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b335c-105">DESCRIPTION</span></span>
<span data-ttu-id="b335c-106">**Add-AzApplicationGatewayCustomError** cmdlet은 사용자 지정 오류를 응용 프로그램 게이트웨이의 http 수신기에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="b335c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b335c-107">EXAMPLES</span></span>

### <span data-ttu-id="b335c-108">예제 1: http 수신기 수준에 사용자 지정 오류 추가</span><span class="sxs-lookup"><span data-stu-id="b335c-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="b335c-109">이 명령은 http 상태 코드 502의 사용자 지정 오류를 http 수신기 $listener 01에 추가 하 고 업데이트 된 수신기를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="b335c-110">변수</span><span class="sxs-lookup"><span data-stu-id="b335c-110">PARAMETERS</span></span>

### <span data-ttu-id="b335c-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="b335c-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="b335c-112">Application gateway 고객 오류의 오류 페이지 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b335c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b335c-113">-DefaultProfile</span></span>
<span data-ttu-id="b335c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b335c-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b335c-115">-HttpListener</span></span>
<span data-ttu-id="b335c-116">Application Gateway Http 수신기</span><span class="sxs-lookup"><span data-stu-id="b335c-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b335c-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b335c-117">-StatusCode</span></span>
<span data-ttu-id="b335c-118">응용 프로그램 게이트웨이 고객 오류의 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b335c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b335c-119">CommonParameters</span></span>
<span data-ttu-id="b335c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b335c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b335c-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b335c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b335c-122">입력</span><span class="sxs-lookup"><span data-stu-id="b335c-122">INPUTS</span></span>

### <span data-ttu-id="b335c-123">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b335c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b335c-124">출력</span><span class="sxs-lookup"><span data-stu-id="b335c-124">OUTPUTS</span></span>

### <span data-ttu-id="b335c-125">Microsoft. c. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b335c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b335c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b335c-126">NOTES</span></span>

## <span data-ttu-id="b335c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b335c-127">RELATED LINKS</span></span>

[<span data-ttu-id="b335c-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b335c-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b335c-129">제거-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b335c-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b335c-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b335c-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)