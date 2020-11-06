---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 281a4a0d935d73777f7fdd693f3d32982b2da47a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530006"
---
# <span data-ttu-id="18ae4-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ae4-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="18ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="18ae4-103">응용 프로그램 게이트웨이에 대 한 WAF 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18ae4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18ae4-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ae4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="18ae4-106">**AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet은 Azure application gateway에 대 한 waf (웹 응용 프로그램 방화벽) 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="18ae4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="18ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="18ae4-108">예제 1: 응용 프로그램 게이트웨이에 대 한 웹 응용 프로그램 방화벽 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="18ae4-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="18ae4-109">첫 번째 명령은 규칙 942130 및 규칙 942140을 사용 하지 않도록 설정 된 규칙 그룹에 대 한 새 규칙 그룹 구성 ("요청-942-SQLI")을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="18ae4-110">두 번째 명령은 "요청-921-프로토콜-ATTACK" 이라는 규칙 그룹에 대해 사용할 수 없는 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="18ae4-111">구체적으로는 규칙이 전달 되지 않으므로 규칙 그룹의 모든 규칙이 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="18ae4-112">마지막 명령은 $disabledRuleGroup 1 및 $disabledRuleGroup 2에서 구성한 대로 방화벽 규칙을 사용 하지 않도록 설정한 WAF 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="18ae4-113">새 WAF 구성은 $firewallConfig 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="18ae4-114">변수</span><span class="sxs-lookup"><span data-stu-id="18ae4-114">PARAMETERS</span></span>

### <span data-ttu-id="18ae4-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="18ae4-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="18ae4-116">비활성화 된 규칙 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-116">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-117">-사용</span><span class="sxs-lookup"><span data-stu-id="18ae4-117">-Enabled</span></span>
<span data-ttu-id="18ae4-118">WAF를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-118">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-119">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="18ae4-119">-FirewallMode</span></span>
<span data-ttu-id="18ae4-120">웹 응용 프로그램 방화벽 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="18ae4-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18ae4-122">기능과</span><span class="sxs-lookup"><span data-stu-id="18ae4-122">Detection</span></span>
- <span data-ttu-id="18ae4-123">공격</span><span class="sxs-lookup"><span data-stu-id="18ae4-123">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-124">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="18ae4-124">-RuleSetType</span></span>
<span data-ttu-id="18ae4-125">웹 응용 프로그램 방화벽 규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="18ae4-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="18ae4-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="18ae4-127">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="18ae4-128">-RuleSetVersion</span></span>
<span data-ttu-id="18ae4-129">규칙 집합 유형의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-129">The version of the rule set type.</span></span>
<span data-ttu-id="18ae4-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="18ae4-131">3.0</span><span class="sxs-lookup"><span data-stu-id="18ae4-131">3.0</span></span>
- <span data-ttu-id="18ae4-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="18ae4-132">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-133">-확인</span><span class="sxs-lookup"><span data-stu-id="18ae4-133">-Confirm</span></span>
<span data-ttu-id="18ae4-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ae4-135">-WhatIf</span></span>
<span data-ttu-id="18ae4-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18ae4-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ae4-138">-DefaultProfile</span></span>
<span data-ttu-id="18ae4-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18ae4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ae4-140">CommonParameters</span></span>
<span data-ttu-id="18ae4-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18ae4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ae4-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ae4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ae4-143">입력</span><span class="sxs-lookup"><span data-stu-id="18ae4-143">INPUTS</span></span>

## <span data-ttu-id="18ae4-144">출력</span><span class="sxs-lookup"><span data-stu-id="18ae4-144">OUTPUTS</span></span>

### <span data-ttu-id="18ae4-145">PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="18ae4-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="18ae4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="18ae4-146">NOTES</span></span>

## <span data-ttu-id="18ae4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18ae4-147">RELATED LINKS</span></span>

[<span data-ttu-id="18ae4-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ae4-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="18ae4-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="18ae4-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

