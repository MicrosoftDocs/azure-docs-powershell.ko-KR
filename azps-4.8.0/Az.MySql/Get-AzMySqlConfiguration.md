---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214413"
---
# <span data-ttu-id="47efc-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="47efc-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="47efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47efc-102">SYNOPSIS</span></span>
<span data-ttu-id="47efc-103">서버 구성에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="47efc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47efc-104">SYNTAX</span></span>

### <span data-ttu-id="47efc-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="47efc-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47efc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="47efc-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47efc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47efc-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="47efc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="47efc-108">DESCRIPTION</span></span>
<span data-ttu-id="47efc-109">서버 구성에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="47efc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="47efc-110">EXAMPLES</span></span>

### <span data-ttu-id="47efc-111">예제 1: 지정 된 MySql 서버의 모든 구성 나열</span><span class="sxs-lookup"><span data-stu-id="47efc-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="47efc-112">이 cmdlet은 지정 된 MySql 서버의 모든 구성을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="47efc-113">예제 2: 이름별로 지정 된 MySql 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="47efc-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="47efc-114">이 cmdlet은 이름을 기준으로 지정 된 MySql 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="47efc-115">변수</span><span class="sxs-lookup"><span data-stu-id="47efc-115">PARAMETERS</span></span>

### <span data-ttu-id="47efc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47efc-116">-DefaultProfile</span></span>
<span data-ttu-id="47efc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47efc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47efc-118">-InputObject</span></span>
<span data-ttu-id="47efc-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47efc-120">-이름</span><span class="sxs-lookup"><span data-stu-id="47efc-120">-Name</span></span>
<span data-ttu-id="47efc-121">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47efc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47efc-122">-ResourceGroupName</span></span>
<span data-ttu-id="47efc-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-123">The name of the resource group.</span></span>
<span data-ttu-id="47efc-124">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-124">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47efc-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47efc-125">-ServerName</span></span>
<span data-ttu-id="47efc-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47efc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47efc-127">-SubscriptionId</span></span>
<span data-ttu-id="47efc-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47efc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47efc-129">CommonParameters</span></span>
<span data-ttu-id="47efc-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47efc-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47efc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47efc-132">입력</span><span class="sxs-lookup"><span data-stu-id="47efc-132">INPUTS</span></span>

### <span data-ttu-id="47efc-133">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="47efc-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="47efc-134">출력</span><span class="sxs-lookup"><span data-stu-id="47efc-134">OUTPUTS</span></span>

### <span data-ttu-id="47efc-135">Api20171201. IConfiguration에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="47efc-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="47efc-136">상속자</span><span class="sxs-lookup"><span data-stu-id="47efc-136">NOTES</span></span>

<span data-ttu-id="47efc-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="47efc-137">ALIASES</span></span>

<span data-ttu-id="47efc-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="47efc-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47efc-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47efc-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="47efc-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47efc-141">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="47efc-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47efc-142">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="47efc-143">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="47efc-144">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="47efc-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="47efc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47efc-146">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="47efc-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47efc-148">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="47efc-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="47efc-150">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="47efc-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47efc-152">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47efc-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="47efc-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47efc-153">RELATED LINKS</span></span>
