---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215453"
---
# <span data-ttu-id="44e97-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="44e97-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="44e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44e97-102">SYNOPSIS</span></span>
<span data-ttu-id="44e97-103">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="44e97-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="44e97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44e97-104">SYNTAX</span></span>

### <span data-ttu-id="44e97-105">ByFieldsWithForwardingParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="44e97-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44e97-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44e97-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44e97-107">설명은</span><span class="sxs-lookup"><span data-stu-id="44e97-107">DESCRIPTION</span></span>
<span data-ttu-id="44e97-108">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="44e97-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="44e97-109">예제의</span><span class="sxs-lookup"><span data-stu-id="44e97-109">EXAMPLES</span></span>

### <span data-ttu-id="44e97-110">예제 1: 전달 규칙을 사용 하 여 전방 도어 만들기에 대 한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="44e97-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="44e97-111">예제 2: 리디렉션 규칙을 사용 하 여 전방 문 만들기에 대 한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="44e97-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="44e97-112">전방 도어 생성을 위한 PSRoutingRuleObject 만들기</span><span class="sxs-lookup"><span data-stu-id="44e97-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="44e97-113">변수</span><span class="sxs-lookup"><span data-stu-id="44e97-113">PARAMETERS</span></span>

### <span data-ttu-id="44e97-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="44e97-114">-AcceptedProtocol</span></span>
<span data-ttu-id="44e97-115">이 규칙에 대해 일치 시킬 프로토콜 스키마입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="44e97-116">기본값은 {Https, Http}입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="44e97-117">-BackendPoolName</span></span>
<span data-ttu-id="44e97-118">이 규칙이 회람 되는 BackendPool의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="44e97-119">-CustomForwardingPath</span></span>
<span data-ttu-id="44e97-120">이 규칙과 일치 하는 리소스 경로를 다시 작성 하는 데 사용 되는 사용자 지정 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="44e97-121">들어오는 경로를 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="44e97-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="44e97-122">-CustomFragment</span></span>
<span data-ttu-id="44e97-123">리디렉션 URL에 추가할 조각입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="44e97-124">단편은 # 다음에 오는 URL의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="44e97-125"># .를 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="44e97-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="44e97-126">-CustomHost</span></span>
<span data-ttu-id="44e97-127">리디렉션할 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-127">Host to redirect.</span></span> <span data-ttu-id="44e97-128">들어오는 호스트를 대상 호스트로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="44e97-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="44e97-129">-CustomPath</span></span>
<span data-ttu-id="44e97-130">리디렉션할 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-130">The full path to redirect.</span></span> <span data-ttu-id="44e97-131">경로는 비워 둘 수 없으며/로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="44e97-132">들어오는 경로를 대상 경로로 사용 하려면 비워 두세요.</span><span class="sxs-lookup"><span data-stu-id="44e97-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-133">-CustomQueryString 쿼리</span><span class="sxs-lookup"><span data-stu-id="44e97-133">-CustomQueryString</span></span>
<span data-ttu-id="44e97-134">리디렉션 URL에 배치할 쿼리 문자열 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="44e97-135">이 값을 설정 하면 기존 쿼리 문자열이 바뀝니다. 수신 쿼리 문자열을 보존 하려면 비워 둡니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="44e97-136">쿼리 문자열은 <key>=</span><span class="sxs-lookup"><span data-stu-id="44e97-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="44e97-137">포맷할.</span><span class="sxs-lookup"><span data-stu-id="44e97-137">format.</span></span> <span data-ttu-id="44e97-138">첫 번째?</span><span class="sxs-lookup"><span data-stu-id="44e97-138">The first ?</span></span> <span data-ttu-id="44e97-139">및 &는 자동으로 추가 되므로 맨 앞에 포함 되지 않고 여러 쿼리 문자열을 &와 분리 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e97-140">-DefaultProfile</span></span>
<span data-ttu-id="44e97-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e97-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="44e97-142">-DynamicCompression</span></span>
<span data-ttu-id="44e97-143">캐싱이 설정 된 경우 캐시 된 콘텐츠에 대 한 동적 압축을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="44e97-144">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="44e97-145">-EnableCaching</span></span>
<span data-ttu-id="44e97-146">이 경로에 캐싱을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="44e97-147">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="44e97-148">-EnabledState</span></span>
<span data-ttu-id="44e97-149">이 규칙의 사용 가능 여부</span><span class="sxs-lookup"><span data-stu-id="44e97-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="44e97-150">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="44e97-151">-ForwardingProtocol</span></span>
<span data-ttu-id="44e97-152">이 규칙은 트래픽을 백 엔드로 전달할 때 사용할 프로토콜입니다. 기본값은 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="44e97-153">-FrontDoorName</span></span>
<span data-ttu-id="44e97-154">이 라우팅 규칙이 속한 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="44e97-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="44e97-155">-FrontendEndpointName</span></span>
<span data-ttu-id="44e97-156">이 규칙과 연결 된 프런트 엔드 끝점의 이름</span><span class="sxs-lookup"><span data-stu-id="44e97-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-157">-이름</span><span class="sxs-lookup"><span data-stu-id="44e97-157">-Name</span></span>
<span data-ttu-id="44e97-158">RoutingRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="44e97-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="44e97-159">-PatternToMatch</span></span>
<span data-ttu-id="44e97-160">규칙의 경로 패턴에는 경로 끝/마지막/이후를 제외한 아무 \*도 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="44e97-161">기본값은/\*입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="44e97-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="44e97-163">캐시 키를 형성할 때의 URL 쿼리 용어 처리입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="44e97-164">기본값은 StripAll입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-165">로 RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="44e97-165">-RedirectProtocol</span></span>
<span data-ttu-id="44e97-166">트래픽이 리디렉션되는 대상의 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="44e97-167">기본 값이 MatchRequest입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-168">RedirectType</span><span class="sxs-lookup"><span data-stu-id="44e97-168">-RedirectType</span></span>
<span data-ttu-id="44e97-169">트래픽을 리디렉션하는 데 사용할 규칙의 리디렉션 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="44e97-170">기본 값이 이동 됨</span><span class="sxs-lookup"><span data-stu-id="44e97-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e97-171">-ResourceGroupName</span></span>
<span data-ttu-id="44e97-172">RoutingRule를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="44e97-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="44e97-173">-RulesEngineName</span></span>
<span data-ttu-id="44e97-174">이 경로에 적용할 특정 규칙 엔진 구성에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e97-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e97-175">CommonParameters</span></span>
<span data-ttu-id="44e97-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e97-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e97-177">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44e97-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e97-178">입력</span><span class="sxs-lookup"><span data-stu-id="44e97-178">INPUTS</span></span>

### <span data-ttu-id="44e97-179">않아야</span><span class="sxs-lookup"><span data-stu-id="44e97-179">None</span></span>

## <span data-ttu-id="44e97-180">출력</span><span class="sxs-lookup"><span data-stu-id="44e97-180">OUTPUTS</span></span>

### <span data-ttu-id="44e97-181">FrontDoor. PSRoutingRule/.</span><span class="sxs-lookup"><span data-stu-id="44e97-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="44e97-182">상속자</span><span class="sxs-lookup"><span data-stu-id="44e97-182">NOTES</span></span>

## <span data-ttu-id="44e97-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44e97-183">RELATED LINKS</span></span>

<span data-ttu-id="44e97-184">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="44e97-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>