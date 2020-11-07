---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1e9a97d01fd42bae636d93311b41bc6150394d9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870485"
---
# <span data-ttu-id="6bd0c-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bd0c-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="6bd0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd0c-103">백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6bd0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bd0c-104">SYNTAX</span></span>

### <span data-ttu-id="6bd0c-105">BackendSetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="6bd0c-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bd0c-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd0c-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd0c-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="6bd0c-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd0c-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd0c-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bd0c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6bd0c-109">DESCRIPTION</span></span>
<span data-ttu-id="6bd0c-110">**AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6bd0c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6bd0c-111">EXAMPLES</span></span>

### <span data-ttu-id="6bd0c-112">예제 1: 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열 만들기</span><span class="sxs-lookup"><span data-stu-id="6bd0c-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="6bd0c-113">이 명령은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="6bd0c-114">변수</span><span class="sxs-lookup"><span data-stu-id="6bd0c-114">PARAMETERS</span></span>

### <span data-ttu-id="6bd0c-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6bd0c-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="6bd0c-116">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6bd0c-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6bd0c-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="6bd0c-118">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="6bd0c-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6bd0c-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="6bd0c-120">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="6bd0c-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6bd0c-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="6bd0c-122">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="6bd0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd0c-123">-DefaultProfile</span></span>
<span data-ttu-id="6bd0c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bd0c-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd0c-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="6bd0c-126">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd0c-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6bd0c-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6bd0c-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="6bd0c-128">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="6bd0c-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bd0c-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="6bd0c-130">Application gateway 기본 재작성 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="6bd0c-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="6bd0c-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="6bd0c-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="6bd0c-132">응용 프로그램 게이트웨이 기본 재작성 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="6bd0c-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="6bd0c-133">-이름</span><span class="sxs-lookup"><span data-stu-id="6bd0c-133">-Name</span></span>
<span data-ttu-id="6bd0c-134">이 cmdlet이 만드는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6bd0c-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="6bd0c-135">-PathRules</span></span>
<span data-ttu-id="6bd0c-136">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="6bd0c-137">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="6bd0c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd0c-138">CommonParameters</span></span>
<span data-ttu-id="6bd0c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd0c-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd0c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd0c-141">입력</span><span class="sxs-lookup"><span data-stu-id="6bd0c-141">INPUTS</span></span>

### <span data-ttu-id="6bd0c-142">않아야</span><span class="sxs-lookup"><span data-stu-id="6bd0c-142">None</span></span>

## <span data-ttu-id="6bd0c-143">출력</span><span class="sxs-lookup"><span data-stu-id="6bd0c-143">OUTPUTS</span></span>

### <span data-ttu-id="6bd0c-144">PSApplicationGatewayUrlPathMap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6bd0c-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="6bd0c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6bd0c-145">NOTES</span></span>

## <span data-ttu-id="6bd0c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bd0c-146">RELATED LINKS</span></span>

[<span data-ttu-id="6bd0c-147">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bd0c-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6bd0c-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bd0c-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6bd0c-149">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bd0c-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6bd0c-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6bd0c-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

