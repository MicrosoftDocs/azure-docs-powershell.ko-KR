---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218641"
---
# <span data-ttu-id="71030-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71030-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="71030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71030-102">SYNOPSIS</span></span>
<span data-ttu-id="71030-103">서버 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="71030-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71030-104">SYNTAX</span></span>

### <span data-ttu-id="71030-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="71030-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="71030-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71030-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71030-107">설명은</span><span class="sxs-lookup"><span data-stu-id="71030-107">DESCRIPTION</span></span>
<span data-ttu-id="71030-108">서버 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="71030-109">예제의</span><span class="sxs-lookup"><span data-stu-id="71030-109">EXAMPLES</span></span>

### <span data-ttu-id="71030-110">예제 1: b 2에서 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="71030-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="71030-111">이 명령은 그 아래에 있는 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="71030-112">변수</span><span class="sxs-lookup"><span data-stu-id="71030-112">PARAMETERS</span></span>

### <span data-ttu-id="71030-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71030-113">-AsJob</span></span>
<span data-ttu-id="71030-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="71030-114">Run the command as a job</span></span>

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

### <span data-ttu-id="71030-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71030-115">-DefaultProfile</span></span>
<span data-ttu-id="71030-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71030-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71030-117">-InputObject</span></span>
<span data-ttu-id="71030-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71030-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71030-119">-이름</span><span class="sxs-lookup"><span data-stu-id="71030-119">-Name</span></span>
<span data-ttu-id="71030-120">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71030-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71030-121">-NoWait</span></span>
<span data-ttu-id="71030-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="71030-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71030-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71030-123">-PassThru</span></span>
<span data-ttu-id="71030-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="71030-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71030-125">-ResourceGroupName</span></span>
<span data-ttu-id="71030-126">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="71030-127">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71030-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71030-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71030-128">-ServerName</span></span>
<span data-ttu-id="71030-129">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71030-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71030-130">-SubscriptionId</span></span>
<span data-ttu-id="71030-131">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71030-132">-확인</span><span class="sxs-lookup"><span data-stu-id="71030-132">-Confirm</span></span>
<span data-ttu-id="71030-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71030-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71030-134">-WhatIf</span></span>
<span data-ttu-id="71030-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71030-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71030-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71030-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71030-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71030-137">CommonParameters</span></span>
<span data-ttu-id="71030-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71030-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="71030-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71030-140">입력</span><span class="sxs-lookup"><span data-stu-id="71030-140">INPUTS</span></span>

### <span data-ttu-id="71030-141">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="71030-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="71030-142">출력</span><span class="sxs-lookup"><span data-stu-id="71030-142">OUTPUTS</span></span>

### <span data-ttu-id="71030-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="71030-143">System.Boolean</span></span>

## <span data-ttu-id="71030-144">상속자</span><span class="sxs-lookup"><span data-stu-id="71030-144">NOTES</span></span>

<span data-ttu-id="71030-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="71030-145">ALIASES</span></span>

<span data-ttu-id="71030-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="71030-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71030-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="71030-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71030-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="71030-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71030-149">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="71030-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71030-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="71030-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="71030-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="71030-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="71030-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71030-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="71030-155">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="71030-156">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71030-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="71030-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="71030-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="71030-159">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="71030-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71030-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="71030-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71030-161">RELATED LINKS</span></span>
