---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219158"
---
# <span data-ttu-id="4fa5a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fa5a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="4fa5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fa5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa5a-103">Redis Cache에 설정 되는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="4fa5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fa5a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fa5a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fa5a-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa5a-106">**RuleName** 매개 변수를 제공 하는 경우 **AzRedisCacheFirewallRule** Cmdlet은 Azure Redis Cache에서 지정 된 방화벽 규칙에 대 한 자세한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="4fa5a-107">**이름만** 지정 된 경우이 작업은 해당 Redis 캐시에서 사용할 수 있는 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="4fa5a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4fa5a-108">EXAMPLES</span></span>

### <span data-ttu-id="4fa5a-109">예제 1: 단일 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="4fa5a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="4fa5a-110">이 명령은 mycache 라는 Redis Cache에서 ruleone 이라는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="4fa5a-111">예제 2: 모든 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="4fa5a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="4fa5a-112">이 명령은 Redis Cache 이라는 mycache의 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="4fa5a-113">변수</span><span class="sxs-lookup"><span data-stu-id="4fa5a-113">PARAMETERS</span></span>

### <span data-ttu-id="4fa5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa5a-114">-DefaultProfile</span></span>
<span data-ttu-id="4fa5a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa5a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4fa5a-116">-Name</span></span>
<span data-ttu-id="4fa5a-117">Redis cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-117">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa5a-118">-ResourceGroupName</span></span>
<span data-ttu-id="4fa5a-119">캐시가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa5a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4fa5a-120">-RuleName</span></span>
<span data-ttu-id="4fa5a-121">방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-121">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa5a-122">CommonParameters</span></span>
<span data-ttu-id="4fa5a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa5a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa5a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa5a-125">입력</span><span class="sxs-lookup"><span data-stu-id="4fa5a-125">INPUTS</span></span>

### <span data-ttu-id="4fa5a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fa5a-126">System.String</span></span>

## <span data-ttu-id="4fa5a-127">출력</span><span class="sxs-lookup"><span data-stu-id="4fa5a-127">OUTPUTS</span></span>

### <span data-ttu-id="4fa5a-128">PSRedisFirewallRule. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="4fa5a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="4fa5a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4fa5a-129">NOTES</span></span>

## <span data-ttu-id="4fa5a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fa5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4fa5a-131">새로운 AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fa5a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="4fa5a-132">제거-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fa5a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="4fa5a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fa5a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4fa5a-134">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fa5a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4fa5a-135">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fa5a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4fa5a-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4fa5a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)