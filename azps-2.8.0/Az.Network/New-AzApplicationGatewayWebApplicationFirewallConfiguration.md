---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: cb66bda25d1353fcfaac732588817ce515fef746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870477"
---
# <span data-ttu-id="126e3-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="126e3-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="126e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="126e3-102">SYNOPSIS</span></span>
<span data-ttu-id="126e3-103">응용 프로그램 게이트웨이에 대 한 WAF 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="126e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="126e3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="126e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="126e3-105">DESCRIPTION</span></span>
<span data-ttu-id="126e3-106">**AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet은 Azure application gateway에 대 한 waf (웹 응용 프로그램 방화벽) 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="126e3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="126e3-107">EXAMPLES</span></span>

### <span data-ttu-id="126e3-108">예제 1: 응용 프로그램 게이트웨이에 대 한 웹 응용 프로그램 방화벽 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="126e3-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="126e3-109">첫 번째 명령은 규칙 942130 및 규칙 942140을 사용 하지 않도록 설정 된 규칙 그룹에 대 한 새 규칙 그룹 구성 ("요청-942-SQLI")을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="126e3-110">두 번째 명령은 "요청-921-프로토콜-ATTACK" 이라는 규칙 그룹에 대해 사용할 수 없는 규칙 그룹 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="126e3-111">구체적으로는 규칙이 전달 되지 않으므로 규칙 그룹의 모든 규칙이 비활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="126e3-112">마지막 명령은 $disabledRuleGroup 1 및 $disabledRuleGroup 2에서 구성한 대로 방화벽 규칙을 사용 하지 않도록 설정한 WAF 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="126e3-113">새 WAF 구성은 $firewallConfig 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="126e3-114">변수</span><span class="sxs-lookup"><span data-stu-id="126e3-114">PARAMETERS</span></span>

### <span data-ttu-id="126e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126e3-115">-DefaultProfile</span></span>
<span data-ttu-id="126e3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="126e3-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="126e3-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="126e3-118">비활성화 된 규칙 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126e3-119">-사용</span><span class="sxs-lookup"><span data-stu-id="126e3-119">-Enabled</span></span>
<span data-ttu-id="126e3-120">WAF를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="126e3-121">-제외</span><span class="sxs-lookup"><span data-stu-id="126e3-121">-Exclusion</span></span>
<span data-ttu-id="126e3-122">제외 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126e3-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="126e3-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="126e3-124">최대 파일 업로드 제한 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126e3-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="126e3-125">-FirewallMode</span></span>
<span data-ttu-id="126e3-126">웹 응용 프로그램 방화벽 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="126e3-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="126e3-128">기능과</span><span class="sxs-lookup"><span data-stu-id="126e3-128">Detection</span></span>
- <span data-ttu-id="126e3-129">공격</span><span class="sxs-lookup"><span data-stu-id="126e3-129">Prevention</span></span>

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

### <span data-ttu-id="126e3-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="126e3-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="126e3-131">최대 요청 본문 크기 (KB)입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126e3-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="126e3-132">-RequestBodyCheck</span></span>
<span data-ttu-id="126e3-133">요청 본문의 확인 여부</span><span class="sxs-lookup"><span data-stu-id="126e3-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126e3-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="126e3-134">-RuleSetType</span></span>
<span data-ttu-id="126e3-135">웹 응용 프로그램 방화벽 규칙 집합의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="126e3-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="126e3-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="126e3-137">OWASP</span></span>

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

### <span data-ttu-id="126e3-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="126e3-138">-RuleSetVersion</span></span>
<span data-ttu-id="126e3-139">규칙 집합 유형의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126e3-140">-확인</span><span class="sxs-lookup"><span data-stu-id="126e3-140">-Confirm</span></span>
<span data-ttu-id="126e3-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126e3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126e3-142">-WhatIf</span></span>
<span data-ttu-id="126e3-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="126e3-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126e3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126e3-145">CommonParameters</span></span>
<span data-ttu-id="126e3-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="126e3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126e3-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126e3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126e3-148">입력</span><span class="sxs-lookup"><span data-stu-id="126e3-148">INPUTS</span></span>

### <span data-ttu-id="126e3-149">않아야</span><span class="sxs-lookup"><span data-stu-id="126e3-149">None</span></span>

## <span data-ttu-id="126e3-150">출력</span><span class="sxs-lookup"><span data-stu-id="126e3-150">OUTPUTS</span></span>

### <span data-ttu-id="126e3-151">PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="126e3-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="126e3-152">상속자</span><span class="sxs-lookup"><span data-stu-id="126e3-152">NOTES</span></span>

## <span data-ttu-id="126e3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="126e3-153">RELATED LINKS</span></span>

[<span data-ttu-id="126e3-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="126e3-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="126e3-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="126e3-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

