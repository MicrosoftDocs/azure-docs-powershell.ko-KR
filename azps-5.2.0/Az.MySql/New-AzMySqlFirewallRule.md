---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 67ef03656b97514d1d39ae72f0f0d52d5b302619
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336345"
---
# <span data-ttu-id="ab819-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab819-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="ab819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab819-102">SYNOPSIS</span></span>
<span data-ttu-id="ab819-103">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ab819-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab819-104">SYNTAX</span></span>

### <span data-ttu-id="ab819-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab819-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab819-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="ab819-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ab819-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab819-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab819-108">설명</span><span class="sxs-lookup"><span data-stu-id="ab819-108">DESCRIPTION</span></span>
<span data-ttu-id="ab819-109">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ab819-110">예제</span><span class="sxs-lookup"><span data-stu-id="ab819-110">EXAMPLES</span></span>

### <span data-ttu-id="ab819-111">예제 1: 새 MySql 서버 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ab819-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="ab819-112">이 cmdlet은 MySql 서버 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="ab819-113">예제 2: -ClientIPAddress를 사용하여 새 MySql 방화벽 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="ab819-114">이 cmdlet은 -ClientIPAddress를 사용하여 MySql 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="ab819-115">예제 3: 모든 IPS를 허용하는 새 MySql 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ab819-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="ab819-116">이 cmdlet은 모든 IPS를 허용하는 새 MySql 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="ab819-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab819-117">PARAMETERS</span></span>

### <span data-ttu-id="ab819-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="ab819-118">-AllowAll</span></span>
<span data-ttu-id="ab819-119">0.0.0.0에서 255.255.255.255.255까지 모든 범위의 IPS를 허용하도록 제시합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab819-120">-AsJob</span></span>
<span data-ttu-id="ab819-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ab819-121">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab819-122">-ClientIPAddress</span></span>
<span data-ttu-id="ab819-123">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="ab819-124">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab819-125">-DefaultProfile</span></span>
<span data-ttu-id="ab819-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab819-127">-EndIPAddress</span></span>
<span data-ttu-id="ab819-128">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="ab819-129">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ab819-130">-Name</span></span>
<span data-ttu-id="ab819-131">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="ab819-132">지정하지 않으면 기본값이 정의되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="ab819-133">AllowAll이 있는 경우 기본 이름은 AllowAll_yyyy-MM-dd_HH-mm-ss입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ab819-134">-NoWait</span></span>
<span data-ttu-id="ab819-135">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ab819-135">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab819-136">-ResourceGroupName</span></span>
<span data-ttu-id="ab819-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-137">The name of the resource group.</span></span>
<span data-ttu-id="ab819-138">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ab819-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ab819-139">-ServerName</span></span>
<span data-ttu-id="ab819-140">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-140">The name of the server.</span></span>

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

### <span data-ttu-id="ab819-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab819-141">-StartIPAddress</span></span>
<span data-ttu-id="ab819-142">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="ab819-143">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab819-144">-SubscriptionId</span></span>
<span data-ttu-id="ab819-145">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab819-146">-Confirm</span></span>
<span data-ttu-id="ab819-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab819-148">-WhatIf</span></span>
<span data-ttu-id="ab819-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ab819-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab819-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab819-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab819-151">CommonParameters</span></span>
<span data-ttu-id="ab819-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab819-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab819-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab819-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab819-154">입력</span><span class="sxs-lookup"><span data-stu-id="ab819-154">INPUTS</span></span>

## <span data-ttu-id="ab819-155">출력</span><span class="sxs-lookup"><span data-stu-id="ab819-155">OUTPUTS</span></span>

### <span data-ttu-id="ab819-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab819-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ab819-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab819-157">NOTES</span></span>

<span data-ttu-id="ab819-158">별칭</span><span class="sxs-lookup"><span data-stu-id="ab819-158">ALIASES</span></span>

## <span data-ttu-id="ab819-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab819-159">RELATED LINKS</span></span>
