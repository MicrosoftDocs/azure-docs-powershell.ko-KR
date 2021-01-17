---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332150"
---
# <span data-ttu-id="82d71-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="82d71-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="82d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d71-102">SYNOPSIS</span></span>
<span data-ttu-id="82d71-103">서비스가 종속된 외부 리소스에 대한 네트워크 연결 상태를 진단합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="82d71-104">구문</span><span class="sxs-lookup"><span data-stu-id="82d71-104">SYNTAX</span></span>

### <span data-ttu-id="82d71-105">진단(기본값)</span><span class="sxs-lookup"><span data-stu-id="82d71-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="82d71-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="82d71-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82d71-107">설명</span><span class="sxs-lookup"><span data-stu-id="82d71-107">DESCRIPTION</span></span>
<span data-ttu-id="82d71-108">서비스가 종속된 외부 리소스에 대한 네트워크 연결 상태를 진단합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="82d71-109">예제</span><span class="sxs-lookup"><span data-stu-id="82d71-109">EXAMPLES</span></span>

### <span data-ttu-id="82d71-110">예제 1: 외부 리소스에 대한 네트워크 연결 진단 표시</span><span class="sxs-lookup"><span data-stu-id="82d71-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="82d71-111">위의 명령은 클러스터 "testnewkustocluster"가 종속된 외부 리소스에 대한 네트워크 연결 상태를 진단합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="82d71-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82d71-112">PARAMETERS</span></span>

### <span data-ttu-id="82d71-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82d71-113">-AsJob</span></span>
<span data-ttu-id="82d71-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="82d71-114">Run the command as a job</span></span>

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

### <span data-ttu-id="82d71-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="82d71-115">-ClusterName</span></span>
<span data-ttu-id="82d71-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d71-117">-DefaultProfile</span></span>
<span data-ttu-id="82d71-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82d71-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82d71-119">-InputObject</span></span>
<span data-ttu-id="82d71-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="82d71-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82d71-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82d71-121">-NoWait</span></span>
<span data-ttu-id="82d71-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="82d71-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="82d71-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d71-123">-ResourceGroupName</span></span>
<span data-ttu-id="82d71-124">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d71-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82d71-125">-SubscriptionId</span></span>
<span data-ttu-id="82d71-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="82d71-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d71-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82d71-128">-Confirm</span></span>
<span data-ttu-id="82d71-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82d71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82d71-130">-WhatIf</span></span>
<span data-ttu-id="82d71-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82d71-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82d71-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82d71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d71-133">CommonParameters</span></span>
<span data-ttu-id="82d71-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d71-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82d71-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d71-136">입력</span><span class="sxs-lookup"><span data-stu-id="82d71-136">INPUTS</span></span>

### <span data-ttu-id="82d71-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="82d71-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="82d71-138">출력</span><span class="sxs-lookup"><span data-stu-id="82d71-138">OUTPUTS</span></span>

### <span data-ttu-id="82d71-139">System.String</span><span class="sxs-lookup"><span data-stu-id="82d71-139">System.String</span></span>

## <span data-ttu-id="82d71-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82d71-140">NOTES</span></span>

<span data-ttu-id="82d71-141">별칭</span><span class="sxs-lookup"><span data-stu-id="82d71-141">ALIASES</span></span>

<span data-ttu-id="82d71-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="82d71-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82d71-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82d71-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82d71-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82d71-145">INPUTOBJECT: <IKustoIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="82d71-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="82d71-146">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="82d71-147">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="82d71-148">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="82d71-149">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="82d71-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="82d71-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="82d71-151">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="82d71-152">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="82d71-153">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="82d71-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="82d71-155">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="82d71-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="82d71-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82d71-156">RELATED LINKS</span></span>
