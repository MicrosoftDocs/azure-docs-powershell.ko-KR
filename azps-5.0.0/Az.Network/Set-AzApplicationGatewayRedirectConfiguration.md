---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 87013db1f8bdff42fd34f28d45d5998d056aab40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218516"
---
# <span data-ttu-id="53e26-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e26-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="53e26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53e26-102">SYNOPSIS</span></span>
<span data-ttu-id="53e26-103">기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="53e26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53e26-104">SYNTAX</span></span>

### <span data-ttu-id="53e26-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53e26-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53e26-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="53e26-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53e26-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="53e26-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53e26-108">설명은</span><span class="sxs-lookup"><span data-stu-id="53e26-108">DESCRIPTION</span></span>
<span data-ttu-id="53e26-109">**AzApplicationGatewayRequestRoutingRule Cmdlet은** 리디렉션 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="53e26-110">예제의</span><span class="sxs-lookup"><span data-stu-id="53e26-110">EXAMPLES</span></span>

### <span data-ttu-id="53e26-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="53e26-111">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="53e26-112">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="53e26-113">두 번째 명령은 application gateway에 대 한 리디렉션 구성을 수정 하 여 형식 영구 리디렉션 및 대상 url을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

### <span data-ttu-id="53e26-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="53e26-114">Example 2</span></span>

<span data-ttu-id="53e26-115">기존 응용 프로그램 게이트웨이에서 리디렉션 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-115">Sets the redirect configuration on an existing Application Gateway.</span></span> <span data-ttu-id="53e26-116">생성</span><span class="sxs-lookup"><span data-stu-id="53e26-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -IncludePath $false -IncludeQueryString $false -Name 'RedirectConfig01' -RedirectType Permanent -TargetListener <PSApplicationGatewayHttpListener>
```

## <span data-ttu-id="53e26-117">변수</span><span class="sxs-lookup"><span data-stu-id="53e26-117">PARAMETERS</span></span>

### <span data-ttu-id="53e26-118">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53e26-118">-ApplicationGateway</span></span>
<span data-ttu-id="53e26-119">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53e26-119">The applicationGateway</span></span>

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

### <span data-ttu-id="53e26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e26-120">-DefaultProfile</span></span>
<span data-ttu-id="53e26-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53e26-122">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="53e26-122">-IncludePath</span></span>
<span data-ttu-id="53e26-123">리디렉션된 url의 포함 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-123">Include path in the redirected url.</span></span>
<span data-ttu-id="53e26-124">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e26-125">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="53e26-125">-IncludeQueryString</span></span>
<span data-ttu-id="53e26-126">리디렉션된 url에 쿼리 문자열을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-126">Include query string in the redirected url.</span></span>
<span data-ttu-id="53e26-127">기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-127">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e26-128">-이름</span><span class="sxs-lookup"><span data-stu-id="53e26-128">-Name</span></span>
<span data-ttu-id="53e26-129">리디렉션 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-129">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="53e26-130">RedirectType</span><span class="sxs-lookup"><span data-stu-id="53e26-130">-RedirectType</span></span>
<span data-ttu-id="53e26-131">리디렉션 유형</span><span class="sxs-lookup"><span data-stu-id="53e26-131">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e26-132">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="53e26-132">-TargetListener</span></span>
<span data-ttu-id="53e26-133">요청을 리디렉션할 HTTP 수신기</span><span class="sxs-lookup"><span data-stu-id="53e26-133">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e26-134">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="53e26-134">-TargetListenerID</span></span>
<span data-ttu-id="53e26-135">요청을 리디렉션할 HTTP 수신기의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-135">ID of HTTP listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e26-136">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="53e26-136">-TargetUrl</span></span>
<span data-ttu-id="53e26-137">대상 URL 리디렉션</span><span class="sxs-lookup"><span data-stu-id="53e26-137">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53e26-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e26-138">CommonParameters</span></span>
<span data-ttu-id="53e26-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53e26-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e26-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e26-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e26-141">입력</span><span class="sxs-lookup"><span data-stu-id="53e26-141">INPUTS</span></span>

### <span data-ttu-id="53e26-142">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53e26-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53e26-143">출력</span><span class="sxs-lookup"><span data-stu-id="53e26-143">OUTPUTS</span></span>

### <span data-ttu-id="53e26-144">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53e26-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53e26-145">상속자</span><span class="sxs-lookup"><span data-stu-id="53e26-145">NOTES</span></span>

## <span data-ttu-id="53e26-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53e26-146">RELATED LINKS</span></span>

[<span data-ttu-id="53e26-147">추가-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e26-147">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="53e26-148">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e26-148">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="53e26-149">새로운 AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e26-149">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="53e26-150">제거-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e26-150">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)