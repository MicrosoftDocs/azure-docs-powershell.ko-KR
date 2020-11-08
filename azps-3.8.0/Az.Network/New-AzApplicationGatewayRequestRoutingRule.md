---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 8fc8f6785e9b6eda55615fb1e2ececbaf9ab0349
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044787"
---
# <span data-ttu-id="6e33e-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e33e-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6e33e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e33e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e33e-103">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6e33e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e33e-104">SYNTAX</span></span>

### <span data-ttu-id="6e33e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e33e-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e33e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6e33e-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e33e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e33e-107">DESCRIPTION</span></span>
<span data-ttu-id="6e33e-108">**AzApplicationGatewayRequestRoutingRule Cmdlet은** Azure application gateway에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="6e33e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e33e-109">EXAMPLES</span></span>

### <span data-ttu-id="6e33e-110">예제 1: 응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="6e33e-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6e33e-111">이 명령은 Rule01 이라는 기본 요청 라우팅 규칙을 만들고 그 결과를 $Rule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="6e33e-112">변수</span><span class="sxs-lookup"><span data-stu-id="6e33e-112">PARAMETERS</span></span>

### <span data-ttu-id="6e33e-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6e33e-113">-BackendAddressPool</span></span>
<span data-ttu-id="6e33e-114">만들 요청 라우팅 규칙에 대 한 백 엔드 주소 풀을 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33e-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6e33e-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="6e33e-116">만들려는 요청 라우팅 규칙의 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="6e33e-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6e33e-117">-BackendHttpSettings</span></span>
<span data-ttu-id="6e33e-118">만들 요청 라우팅 규칙에 대 한 개체의 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33e-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6e33e-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6e33e-120">만들려는 요청 라우팅 규칙의 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="6e33e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e33e-121">-DefaultProfile</span></span>
<span data-ttu-id="6e33e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e33e-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6e33e-123">-HttpListener</span></span>
<span data-ttu-id="6e33e-124">만들 요청 라우팅 규칙에 대 한 백 엔드 HTTP 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6e33e-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="6e33e-125">-HttpListenerId</span></span>
<span data-ttu-id="6e33e-126">만들 요청 라우팅 규칙에 대 한 백 엔드 HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="6e33e-127">-이름</span><span class="sxs-lookup"><span data-stu-id="6e33e-127">-Name</span></span>
<span data-ttu-id="6e33e-128">이 cmdlet이 만드는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6e33e-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e33e-129">-RedirectConfiguration</span></span>
<span data-ttu-id="6e33e-130">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e33e-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33e-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6e33e-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="6e33e-132">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6e33e-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e33e-133">-RewriteRuleSet</span></span>
<span data-ttu-id="6e33e-134">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e33e-134">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33e-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6e33e-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="6e33e-136">응용 프로그램 게이트웨이 RewriteRuleSet의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6e33e-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6e33e-137">-RuleType</span></span>
<span data-ttu-id="6e33e-138">요청 라우팅 규칙의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-138">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33e-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6e33e-139">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33e-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6e33e-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6e33e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e33e-141">CommonParameters</span></span>
<span data-ttu-id="6e33e-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e33e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e33e-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e33e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e33e-144">입력</span><span class="sxs-lookup"><span data-stu-id="6e33e-144">INPUTS</span></span>

### <span data-ttu-id="6e33e-145">않아야</span><span class="sxs-lookup"><span data-stu-id="6e33e-145">None</span></span>

## <span data-ttu-id="6e33e-146">출력</span><span class="sxs-lookup"><span data-stu-id="6e33e-146">OUTPUTS</span></span>

### <span data-ttu-id="6e33e-147">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6e33e-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6e33e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6e33e-148">NOTES</span></span>

## <span data-ttu-id="6e33e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e33e-149">RELATED LINKS</span></span>

[<span data-ttu-id="6e33e-150">추가-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e33e-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e33e-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e33e-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e33e-152">제거-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e33e-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6e33e-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6e33e-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

