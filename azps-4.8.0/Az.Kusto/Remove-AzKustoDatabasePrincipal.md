---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214496"
---
# <span data-ttu-id="f504c-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f504c-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f504c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f504c-102">SYNOPSIS</span></span>
<span data-ttu-id="f504c-103">데이터베이스 보안 주체 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="f504c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f504c-104">SYNTAX</span></span>

### <span data-ttu-id="f504c-105">RemoveExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f504c-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f504c-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f504c-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f504c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f504c-107">DESCRIPTION</span></span>
<span data-ttu-id="f504c-108">데이터베이스 보안 주체 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="f504c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f504c-109">EXAMPLES</span></span>

### <span data-ttu-id="f504c-110">예제 1: 데이터베이스 사용자 권한 제거</span><span class="sxs-lookup"><span data-stu-id="f504c-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f504c-111">위의 명령은 데이터베이스 사용자 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="f504c-112">변수</span><span class="sxs-lookup"><span data-stu-id="f504c-112">PARAMETERS</span></span>

### <span data-ttu-id="f504c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f504c-113">-ClusterName</span></span>
<span data-ttu-id="f504c-114">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f504c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f504c-115">-DatabaseName</span></span>
<span data-ttu-id="f504c-116">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f504c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f504c-117">-DefaultProfile</span></span>
<span data-ttu-id="f504c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f504c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f504c-119">-InputObject</span></span>
<span data-ttu-id="f504c-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f504c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f504c-121">-ResourceGroupName</span></span>
<span data-ttu-id="f504c-122">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f504c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f504c-123">-SubscriptionId</span></span>
<span data-ttu-id="f504c-124">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f504c-125">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f504c-126">-값</span><span class="sxs-lookup"><span data-stu-id="f504c-126">-Value</span></span>
<span data-ttu-id="f504c-127">데이터베이스 주체에 대 한 Kusto의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="f504c-128">생성 하려면 값 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f504c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="f504c-129">-Confirm</span></span>
<span data-ttu-id="f504c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f504c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f504c-131">-WhatIf</span></span>
<span data-ttu-id="f504c-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f504c-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f504c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f504c-134">CommonParameters</span></span>
<span data-ttu-id="f504c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f504c-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f504c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f504c-137">입력</span><span class="sxs-lookup"><span data-stu-id="f504c-137">INPUTS</span></span>

### <span data-ttu-id="f504c-138">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="f504c-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f504c-139">출력</span><span class="sxs-lookup"><span data-stu-id="f504c-139">OUTPUTS</span></span>

### <span data-ttu-id="f504c-140">Api20200614. i a PowerShell. IDatabasePrincipal.</span><span class="sxs-lookup"><span data-stu-id="f504c-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="f504c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="f504c-141">NOTES</span></span>

<span data-ttu-id="f504c-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="f504c-142">ALIASES</span></span>

<span data-ttu-id="f504c-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f504c-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f504c-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f504c-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="f504c-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f504c-146">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f504c-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f504c-147">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f504c-148">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f504c-149">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f504c-150">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f504c-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="f504c-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f504c-152">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="f504c-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f504c-153">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f504c-154">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f504c-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f504c-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f504c-157">값 <IDatabasePrincipal [] >: Kusto 데이터베이스 사용자의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="f504c-158">`Name <String>`: 데이터베이스 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="f504c-159">`Role <DatabasePrincipalRole>`: 데이터베이스 주체 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="f504c-160">`Type <DatabasePrincipalType>`: 데이터베이스 보안 주체 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="f504c-161">`[AppId <String>]`: 응용 프로그램 id-응용 프로그램 보안 주체 유형에만 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="f504c-162">`[Email <String>]`: 데이터베이스 보안 주체 전자 메일 (있는 경우)</span><span class="sxs-lookup"><span data-stu-id="f504c-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="f504c-163">`[Fqn <String>]`: 데이터베이스 주체 정규화 된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504c-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="f504c-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f504c-164">RELATED LINKS</span></span>
