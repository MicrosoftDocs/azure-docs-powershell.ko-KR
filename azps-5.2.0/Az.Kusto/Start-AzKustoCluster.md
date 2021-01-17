---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350913"
---
# <span data-ttu-id="1cdd0-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="1cdd0-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="1cdd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cdd0-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdd0-103">Kusto 클러스터를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="1cdd0-104">구문</span><span class="sxs-lookup"><span data-stu-id="1cdd0-104">SYNTAX</span></span>

### <span data-ttu-id="1cdd0-105">시작(기본값)</span><span class="sxs-lookup"><span data-stu-id="1cdd0-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1cdd0-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1cdd0-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1cdd0-107">설명</span><span class="sxs-lookup"><span data-stu-id="1cdd0-107">DESCRIPTION</span></span>
<span data-ttu-id="1cdd0-108">Kusto 클러스터를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="1cdd0-109">예제</span><span class="sxs-lookup"><span data-stu-id="1cdd0-109">EXAMPLES</span></span>

### <span data-ttu-id="1cdd0-110">예제 1: Kusto 클러스터 시작</span><span class="sxs-lookup"><span data-stu-id="1cdd0-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="1cdd0-111">위의 명령은 Kusto 클러스터를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="1cdd0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cdd0-112">PARAMETERS</span></span>

### <span data-ttu-id="1cdd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cdd0-113">-AsJob</span></span>
<span data-ttu-id="1cdd0-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1cdd0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1cdd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdd0-115">-DefaultProfile</span></span>
<span data-ttu-id="1cdd0-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cdd0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cdd0-117">-InputObject</span></span>
<span data-ttu-id="1cdd0-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdd0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1cdd0-119">-Name</span></span>
<span data-ttu-id="1cdd0-120">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdd0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1cdd0-121">-NoWait</span></span>
<span data-ttu-id="1cdd0-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1cdd0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1cdd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cdd0-123">-PassThru</span></span>
<span data-ttu-id="1cdd0-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1cdd0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cdd0-125">-ResourceGroupName</span></span>
<span data-ttu-id="1cdd0-126">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdd0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cdd0-127">-SubscriptionId</span></span>
<span data-ttu-id="1cdd0-128">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1cdd0-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdd0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cdd0-130">-Confirm</span></span>
<span data-ttu-id="1cdd0-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cdd0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cdd0-132">-WhatIf</span></span>
<span data-ttu-id="1cdd0-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1cdd0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cdd0-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cdd0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdd0-135">CommonParameters</span></span>
<span data-ttu-id="1cdd0-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdd0-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdd0-138">입력</span><span class="sxs-lookup"><span data-stu-id="1cdd0-138">INPUTS</span></span>

### <span data-ttu-id="1cdd0-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1cdd0-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1cdd0-140">출력</span><span class="sxs-lookup"><span data-stu-id="1cdd0-140">OUTPUTS</span></span>

### <span data-ttu-id="1cdd0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cdd0-141">System.Boolean</span></span>

## <span data-ttu-id="1cdd0-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1cdd0-142">NOTES</span></span>

<span data-ttu-id="1cdd0-143">별칭</span><span class="sxs-lookup"><span data-stu-id="1cdd0-143">ALIASES</span></span>

<span data-ttu-id="1cdd0-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1cdd0-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1cdd0-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1cdd0-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1cdd0-147">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1cdd0-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1cdd0-148">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1cdd0-149">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1cdd0-150">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1cdd0-151">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1cdd0-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1cdd0-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1cdd0-153">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1cdd0-154">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1cdd0-155">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1cdd0-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1cdd0-157">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1cdd0-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cdd0-158">RELATED LINKS</span></span>
