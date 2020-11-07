---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 970ae86a9664dad32e7c91c35abb17cd086a0130
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870330"
---
# <span data-ttu-id="00b68-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00b68-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="00b68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b68-102">SYNOPSIS</span></span>
<span data-ttu-id="00b68-103">백 엔드 서버 풀에 URL 경로 매핑 배열을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="00b68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00b68-104">SYNTAX</span></span>

### <span data-ttu-id="00b68-105">BackendSetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="00b68-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00b68-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00b68-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00b68-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="00b68-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00b68-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00b68-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00b68-109">설명은</span><span class="sxs-lookup"><span data-stu-id="00b68-109">DESCRIPTION</span></span>
<span data-ttu-id="00b68-110">**Add-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 URL 경로 매핑 배열을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="00b68-111">예제의</span><span class="sxs-lookup"><span data-stu-id="00b68-111">EXAMPLES</span></span>

### <span data-ttu-id="00b68-112">예제 1: 응용 프로그램 게이트웨이에 대 한 URL 경로 매핑을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="00b68-113">첫 번째 명령은 appGwName 이라는 응용 프로그램 게이트웨이를 가져와이를 $appgw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="00b68-114">두 번째 명령은 백 엔드 주소 풀을 가져와 $pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="00b68-115">세 번째 명령은 백 엔드 http 설정을 가져와 $poolSettings 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="00b68-116">네 번째 명령은 rule01 이라는 새 경로 규칙 구성을 만들고이를 $pathRule 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="00b68-117">다섯 번째 명령은 url01 이라는 url 경로 매핑 구성을 응용 프로그램 게이트웨이에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="00b68-118">여섯 번째 명령은 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="00b68-119">변수</span><span class="sxs-lookup"><span data-stu-id="00b68-119">PARAMETERS</span></span>

### <span data-ttu-id="00b68-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00b68-120">-ApplicationGateway</span></span>
<span data-ttu-id="00b68-121">이 cmdlet이 URL 경로 맵 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="00b68-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="00b68-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="00b68-123">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="00b68-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="00b68-125">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00b68-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="00b68-127">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="00b68-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="00b68-129">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b68-130">-DefaultProfile</span></span>
<span data-ttu-id="00b68-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b68-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00b68-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="00b68-133">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00b68-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="00b68-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="00b68-135">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00b68-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="00b68-137">Application gateway 기본 재작성 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="00b68-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="00b68-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="00b68-139">응용 프로그램 게이트웨이 기본 재작성 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="00b68-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-140">-이름</span><span class="sxs-lookup"><span data-stu-id="00b68-140">-Name</span></span>
<span data-ttu-id="00b68-141">이 cmdlet가 백 엔드 서버 풀에 추가 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="00b68-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="00b68-142">-PathRules</span></span>
<span data-ttu-id="00b68-143">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="00b68-144">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00b68-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b68-145">CommonParameters</span></span>
<span data-ttu-id="00b68-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b68-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b68-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b68-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b68-148">입력</span><span class="sxs-lookup"><span data-stu-id="00b68-148">INPUTS</span></span>

### <span data-ttu-id="00b68-149">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00b68-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00b68-150">출력</span><span class="sxs-lookup"><span data-stu-id="00b68-150">OUTPUTS</span></span>

### <span data-ttu-id="00b68-151">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00b68-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00b68-152">상속자</span><span class="sxs-lookup"><span data-stu-id="00b68-152">NOTES</span></span>

## <span data-ttu-id="00b68-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00b68-153">RELATED LINKS</span></span>

[<span data-ttu-id="00b68-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00b68-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00b68-155">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00b68-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00b68-156">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00b68-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00b68-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00b68-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

